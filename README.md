# JavaScript Code

 1. **Adding Event Listeners to a Button**
```javascript
document.querySelectorAll(".drum")[i].addEventListener("click", function() 
	{ 
		aler("I got clicked"); 
	}
);
```
 2. **Higher Order Functions and Passing Functions as Arguments**
 (Functions that take other functions as input.)
 ex:
```javascript
function add(num1, num2)  { return num1 + num2; }
function subtract(num1, num2)  { return num1 - num2; }
function multiply(num1, num2)  { return num1 * num2;}
function divide(num1, num2)  { return num1 / num2; }
function calculator(num1, num2,  operator)  { return  operator(num1,num2);}
```
3. **Playing Sound in Website**
ex.
```javascript
function playSound(url) {
  const audio = new Audio(url);
  audio.play();
}
```

```xml
<button onclick="playSound('https://your-file.mp3');">Play</button> 
```
 - **JavaScript Object** 
	
 - Object
 ```javascript
 var bellBoy1={
  name:"Timmy",
  age:19,
  hasWorkPermit:true,
  languages:["French","English"]
}
 ```
 - Constructor Function
 ```javascript
 function BellBoy(name,age,hasWorkPermit,languages){
  this.name=name;
  this.age=age;
  this.hasWorkPermit=hasWorkPermit;
  this.languages=languages;
}
```
 - Initalise Object
```javascript
var bellBoyl=new BellBoy("Timmy",19,true,["French","English"]);
 ```
 - Switch Statement in JavaScript
 ```javascript
switch (key) {
    case "w":
      var tom1 = new Audio("sounds/tom-1.mp3");
      tom1.play();
      break;
	case "a":
      var tom2 = new Audio("sounds/tom-2.mp3");
      tom2.play();
      break;
    case "s":
      var tom3 = new Audio('sounds/tom-3.mp3');
      tom3.play();
      break;
    case "d":
      var tom4 = new Audio('sounds/tom-4.mp3');
      tom4.play();
      break;
    case "j":
      var snare = new Audio('sounds/snare.mp3');
      snare.play();
      break;
    case "k":
      var crash = new Audio('sounds/crash.mp3');
      crash.play();
      break;
    case "l":
      var kick = new Audio('sounds/kick-bass.mp3');
      kick.play();
      break;
    default: console.log(key);
  }
 ```
 4. **Methods (dot notation)**
 ```javascript
 var bellBoy1={
  name:"Timmy",
  age:19,
  hasWorkPermit:true,
  languages:["French","English"],
 
  moveSuitcase:function(){
   alert("MayItake your suitcase?");
   pickUpSuitcase();
   move();
 }
 ```
 - Call Method
 ```javascript
 BellBoy.pickUpSuitcase();
 ```
 - Constructor Function
 ex.
 ```javascript
 function BellBoy(name,age,hasWorkPermit,languages){
  this.name=name;
  this.age=age;
  this.hasWorkPermit=hasWorkPermit;
  this.languages=languages;
  this.moveSuitcase=function(){
    alert("MayItake your suitcase?");
    pickUpSuitcase();
    move();
  }
 ```
```javascript
 Constructor Function
	function Audio(fileLocation){
	this.fileLocation=fileLocation;
	this.play=function(){
		// Tap into the audio hardware
		// Check the file at fileLocation exists
		// Check the file at fileLocation isasound file
		// Play the file at fileLocation
		}
}
var tom1=new Audio("sounds/tom-1.mp3");
tom1.play();
```
 5. **Using Keyboard Event Listeners to Check for Key Presses**
 ```javascript
 document.addEventListener("keypress",function(event){
    makeSound(event.key);
});
 ```
 6. **Callbacks and How to Respond to Events**
 ```javascript
document.addEventListener("keypress", function(event) {
	  makeSound(event.key);
	  buttonAnimation(event.key);
});
 ```
 ```javascript
 function buttonAnimation(currentKey) {
  var activeButton = document.querySelector("." + currentKey);
  activeButton.classList.add("pressed");
  setTimeout(function() {
    activeButton.classList.remove("pressed");
  }, 100);
 ```
 ```css
 .pressed {
  box-shadow: 0 3px 4px 0 #DBEDF3;
  opacity: 0.5;
}
 ```
