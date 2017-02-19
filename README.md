<h1>Pizza App</h1>

<h3>Pizza App with local storage</h3>
<h4> How to use: </h4>
```
*Select Options from drop down menu
*Click Add when all of your options for the pizza are correct
*If you want to edit pizza click the edit button
*Edit your choice then click Edit this order
*Then click done editting

```
<h3>Code</h3>
<p>Getting everything to function properly was the hardest part </p>

            
            mc.editTop1 = function($index){
                mc.toppings = mc.latestData();
                var newTopping = {
                crust: mc.editTopping4.unit_name,
                starting: mc.editTopping1.unit_name,
                veggie: mc.editTopping2.unit_name,
                moreMeat: mc.editTopping3.unit_name
            
                };
                mc.toppings.splice($index, 1, newTopping);
                
                return PizzaStorageService.setData('my-storage', angular.toJson(mc.toppings));
            }               
          
