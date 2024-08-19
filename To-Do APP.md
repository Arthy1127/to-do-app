<!DOCTYPE html>
<html lang="en">
<head>
    <title>TO-DO LIST</title>
    <link rel="stylesheet" href="../html/css/index.css">
</head>
<body>
    <div class="container">
        <h1>Simple Todo APP</h1>
        <div>
            <input type="text" id="todo-input" placeholder="ENTER TO-DO LIST">
            <button onclick="addtodo()">add todo</button>
        </div>
        <ul id="todo-list">
             
        </ul>
    </div>

    <script src="../script.js"></script>
    
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #f3e3e3;
    color: white;
    padding: 1em 0;
}
nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}
nav ul li {
    display: inline;
    margin-right: 20px;
}  
nav a {
   text-decoration: none;
   color: white;
}

div {
    padding: 20px;
}

h1 {
    color: #333;
}


body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em 0;
}

#products {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    padding: 20px;
    
}
.product {
    border: 1px solid #ccc;
    border-radius: 8px;
    padding: 10px;
    margin: 10px;
    text-align: center;
}
.product img {
    max-width: 100%;
    height: auto;
    border-radius: 4px;
    box-sizing: border-box;
    box-shadow: 5px 6px 10px rgb(34, 33, 33);

}
.p {
    font-weight: bold;
}
button {
    background-color: #333;
    color: white;
    padding: 8px 12px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 2em 0;
    position: fixed;
    bottom: 0;
    width: 100%;
}
function addtodo(){
    var todoInput=document.getElementById("todo-input");
    var todoText=todoInput.value.trim();

    if(todoText!==""){ 
        var li=document.createElement("li");
        li.textContent=todoText;


var deleteButton=document.createElement("button");
deleteButton.textContent="Delete";
deleteButton.classList.add("delete-btn");
deleteButton.onclick=function(){
    li.remove();
};
li.appendChild(deleteButton);

document.getElementById("todo-list").appendChild(li);

todoInput.value="";

    }
}
