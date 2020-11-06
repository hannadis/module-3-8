
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatile" content="ie=edge" />
    <link rel="stylesheet" href="./style.css" />  
    <title>Document</title>
</head>
<body>
  <h1 class="title">hello world</h1>
  <button onclick="getit()">Shop</button>
  <button class="addListBtn"> click me</button>

  <ul class="name-list">
    <li>Hanna</li>
    <li>stella</li>
    <li>sandra</li>
    <li>maney</li>
    <li>katrin</li>
    <li>ingibjorg</li>
  </ul>
  
  <input class="list-input" type="text" />
  


</body>
 <script src="index.js"></script>
</html>





const text = document.querySelector(".title");
const changeColor = document.querySelector(".changeColor");


text.style.color = "White";
text.style.backgroundColor = "lightBlue";

text.classList.add('.change');

changeColor.addEventListener("click", function() {
    text.classList.toggle("changeColor")
});


//how to get all the list inside the <ul>
const userList = document.querySelector(".name-list");
const listInput = document.querySelector(".list-input");
const addListBtn = document.querySelector(".addListBtn");

 for (user of userList)  { //inside this I can change each user
    user.addEventListener("click", function() { //on a click there will be a function
    this.style.color = "blue"; //everytime I click on the name the color will change 
    });
 }
 


 addListBtn.addEventListener('click', function() {
//create an li out of thin air 
const newLi = document.createElement('LI'); //with create element its possible to create what I want 
const liContent = document.createTextNode(listInput.value);
console.log(listInput.value);
//add the input value inside the new li
newLi.appendChild(liContent);

//attaching the li to the user list 
userList.appendChild(newLi);
 });

