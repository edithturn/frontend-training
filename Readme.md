# SheCodes Basics

# `REPOSITORY IN PROGRESS ...` :carousel_horse: :raising_hand: :tractor:

This repository will containe my notes in the course [SheCodes](https://www.shecodes.io/) FrontEnd Basics , I will sumarize and show my progress in the three weeks.

## **Weekly summary 01** | HTML and CSS

```html
<!-- Html Elements -->

<!-- Titles -->

<h1></h1>
<h2></h2>
<h3></h3>
<h4></h4>
<h5></h5>

<!-- paragraphs -->

<p>Hello World!</p>

<!-- Lists -->

<ul>
  <li>Element one</li>
  <li>Element two</li>
</ul>

<ol>
  <li>Number one</li>
  <li>Number two</li>
</ol>

<!-- Styling -->

<em>Hello world italic!</em> <strong>Hello world bold!</strong>

<!-- Self closing Tags -->

<hr />
<br />
```

## Developer Tools

ColorZilla chrome extension

<p align="center">
  <img width="450" height="150" src="img/colorzilla.png">
</p>

ctrl + Space Bar -> To HTML sample, to get the HTML template

<p align="center">
  <img width="450" height="110" src="img/html-sample.png">
</p>

Prettier extention for Visual Studio Code

<p align="center">
  <img width="450" height="150" src="img/prettier.png">
</p>

Visual Studio Code theme: Dracula or https://vscodethemes.com/

<p align="center">
  <img width="450" height="150" src="img/dracula.png">
</p>

## Homework Workshop Week 01

<img src="img/img.png" width="400" height="500"/> <img src="img/code.png" width="400" height="500"/>

## **Weekly summary 02** | JavaScript

```javascript
document.querySelectorAll("h2");
document.querySelectorAll(".col-sm-4");
```

Change a html elements with input variable clicking a button

```javascript
function validate(country) {
  let name = prompt("What is  your name?");
  let age = prompt("What is  your age?");
  let welcomeMessage = document.querySelector("h1");

  if (age > 18) {
    welcomeMessage.innerHTML = "Hi " + name + " welcome to" + " SheCodes 👩‍💻";
  } else {
    welcomeMessage.innerHTML =
      "Sorry " + name + " you can't apply to" + " SheCodes 👩‍💻";
  }
}
let applyButton = document.querySelector("button");
applyButton.addEventListener("click", validate);
```

Refactoring

```javascript
function canApply() {
  let age = prompt("What is  your age?");
  return age >= 18;
}
function updateHeader(newHeading) {
  let heading = document.querySelector("h1");
  heading.innerHTML = newHeading;
}
function apply() {
  let name = prompt("What is  your name?");
  if (canApply()) {
    updateHeader(`Hi ${name}  welcome to SheCodes 👩‍💻`);
  } else {
    updateHeader(`Sorry ${name}  you can't apply to SheCodes 👩‍💻`);
  }
}

let applyButton = document.querySelector("button");
applyButton.addEventListener("click", apply);
```

## Homework Workshop Week 02

<p align="center">
  <video src="https://user-images.githubusercontent.com/58795858/134788952-c98c5160-8acd-4219-971d-850edd3684b6.mp4">
</p>

JavaScript Code

```javascript
function updateHeader(newHeader) {
  let header = document.querySelector("h1");
  header.innerHTML = newHeader;
}
function evaluateTemperature() {
  let city = prompt("What city do you life in?");
  let temp = prompt("What is the temperature?");
  if (temp < 0) {
    updateHeader(`😩 </br> Currently ${temp}° in ${city} `);
  } else {
    updateHeader(`😃 </br> Currently ${temp}° in ${city} `);
  }
}
let buttonApply = document.querySelector("button");
buttonApply.addEventListener("click", evaluateTemperature);
```
