# Intent:
* Aggreed rules advantages: <br>
    * Code looks uniform
    * Code review should make sure we are following this guide

### Rules:
1) Follow Single resopncibility principle

### Name:
* Revel the *intent*
* Can be long
```C#
//Ex:
//badname:
var output = someMethod();
return output;

//GoodName:
var randomGegneratedNumber = calculateRandomNumber();
return randomGegneratedNumber;
```

### Class:
#### Name: 
* ClassName should be noun or noun phrase
```C#
//Good Classnames:  
OptimoveTemplate
```
* Max methods of class "?" (3)

* Order of properties and methods:
    * properties
    * constructors
    * methods 

    * by access
        * public
        * internal
        * protected internal
        * protected
        * private
    * With in access order by static and non-static
        * static
        * non-static


#### Strcture:
* Organize classes into folder , if 2 or more class can be logically grouped

#### Abstraction:
* Keep the Root class lite
    * Example: 
        * Job class should have only tigger to job, all the business logic should be seperated into different class
        * Controller classes should only handle requests, business logic should be seperated
* Abstract sitecore operations into different classes, so they can be overloaded easily in unit tests    

### Methods:
* Method should be short, One method should only do one job
* Max number of lines in method '?' (20)

### Exception Handling:
* Exception handling is seperation responsibility itself , keep it seperated
* Popup all exceptions to the root class, try not to have exception handling in inner classes

```C#
//Example: This is java way of handling, we can also agree to any common standard
private string TryGetDataFromExacttargetBlaDataExtension(){
    try { 
        GetDataFromExacttargetBlaDataExtension();
    }
    catch (Exception exception)
    {
        //Hanlde Exception
    }
}
```

### Comments:
Comments are like code and need to maintained, which is extra effort. **DO NOT** comment unless necesseary.
* Comment only the business logic behind it.
* DO NOT comment all properties and methods.
* The method/Class flow should be readable enough to understand 
