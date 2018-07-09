### Step 03 Solutions

**`myName`**

~~~
function myName(){
    var myName = 'Elie Schoppik';
    console.log(myName);
}
~~~

**`randomFood`**

~~~
var favoriteFoods = ['pizza', 'ice cream'];
function randomFood(){
    // lets find a random number between 0 and 1 and multiply it by the length of the array. This will give us a number between 0 and 2. If we always round down, we will get either 0 or 1, so we can use Math.floor to round down.
    var randomIndex = Math.floor(Math.random() * favoriteFoods.length);
    console.log(favoriteFoods[randomIndex]);
}
~~~

**`displayOddNumbers`**

~~~
var numbers = [1,2,3,4,5,6,7,8,9,10];
function displayOddNumbers(){
    for(var i = 0; i < numbers.length; i++){
        // if the value we are at in the array is not divisible by 2 (it's an odd number)
        if(numbers[i] % 2 !== 0){
            // print out that value!
            console.log(numbers[i]);
        }
    }
}
~~~

**`displayEvenNumbers`**

~~~
var numbers = [1,2,3,4,5,6,7,8,9,10];
function displayEvenNumbers(){
    for(var i = 0; i < numbers.length; i++){
        // if the value we are at in the array is divisible by 2 (it's an even number)
        if(numbers[i] % 2 === 0){
            // print out that value!
            console.log(numbers[i]);
        }
    }
}
~~~

**`returnFirstOddNumber`**

~~~
var numbers = [1,2,3,4,5,6,7,8,9,10];
function returnFirstOddNumber(){
    for(var i = 0; i < numbers.length; i++){
        if(numbers[i] % 2 !== 0){
            // print out that value, using return gets us out of the function!
            return numbers[i];
        }
    }
}
~~~

**`returnFirstEvenNumber`**

~~~
var numbers = [1,2,3,4,5,6,7,8,9,10];
function returnFirstEvenNumber(){
    for(var i = 0; i < numbers.length; i++){
        if(numbers[i] % 2 === 0){
            // print out that value!
            return numbers[i];
        }
    }
}
~~~

**`returnFirstHalf`**

~~~
var numbers = [1,2,3,4,5,6,7,8,9,10];
function returnFirstHalf(){
    return numbers.slice(0,numbers.length/2);
}
~~~

**`returnSecondHalf`**

~~~
var numbers = [1,2,3,4,5,6,7,8,9,10];
function returnSecondHalf(){
    return numbers.slice(numbers.length/2);
}
~~~
# JS Functions Exercise Solutions

**`add`**

~~~
function add(num1,num2){
    return num1 + num2;
}
~~~

**`subtract`**

~~~
function subtract(num1,num2){
    return num1 - num2;
}
~~~

**`multiply`**

~~~
function multiply(num1,num2){
    return num1 * num2;
}
~~~

**`divide`**

~~~
function divide(num1,num2){
    return num1 / num2;
}
~~~

**`sayHello`**

~~~
var myFirstName = "Elie";
function sayHello(str){
    if(str === myFirstName){
        return "Hello Boss";
    }
    return "Hello " + str;
}
~~~

**`average`**

~~~
function average(arr){
    var total = 0;
    for(var i = 0; i < arr.length; i++){
        total += arr[i];
    }
    return total / arr.length;
}
~~~

**`createStudent`**

~~~
function createStudent(firstName, lastName){
    return {
        firstName: firstName,
        lastName: lastName
    }
}
~~~

**`findStudentByFirstName`**

~~~
// let's first create some students
var tim = createStudent("Tim", "Garcia");
var matt = createStudent("Matt", "Lane");
var elie = createStudent("Elie", "Schoppik");

var students = [tim, matt, elie];

function findStudentByFirstName(name){
    var lowerCasedName = name.toLowerCase();
    for(var i = 0; i < students.length; i++){
        if(students[i].firstName.toLowerCase() === lowerCasedName){
            return true;
        }
    }
    return false;
}
~~~

**`extractEveryThird`**

~~~
function extractEveryThird(arr){
    var newArr = [];
    for(var i = 2; i < arr.length; i += 3){
        newArr.push(arr[i]);
    }
    return newArr;
}
~~~

**`countEvensAndOdds`**

~~~
function countEvensAndOdds(arr){
    var countObj = {
        oddCount: 0,
        evenCount: 0
    }
    for(var i = 0; i < arr.length; i++){
        if(arr[i] % 2 === 0){
            countObj.evenCount++;
        } else {
            countObj.oddCount++;
        }
    }
    return countObj;
}
~~~

**`scope practice`**

~~~
// the first console.log(myVar) outputs "Hello from global"

// the second console.log(myVar) also outputs "Hello from global" (the trickyScopePractice function was not called!)
~~~

**`onlyCapitalLetters`**

~~~
function onlyCapitalLetters(str){
    var newStr = '';
    for(var i = 0; i < str.length; i++){
        if(str[i].charCodeAt(0) < 91 && str[i].charCodeAt(0) > 64 ){
            newStr += str[i];
        }    
    }
    return newStr;
}
~~~
