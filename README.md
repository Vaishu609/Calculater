# Calculater
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- <link rel="stylesheet" href="cal.css"> -->
    <style>
        html,body{
    height: 100%;
    width: 100%;
}

.container{
    text-align: center;
    
}
.button{
    font-size: 20px;
     margin: 0 3px;
    padding: 20px;
    border: 2px solid black;
    border-radius: 9px;
    color:darkslategray;
    
}
button:hover{
    color: rgb(144, 120, 167);
}
.row{
   margin: 8px 0;
}
.row input{
    margin: 10px;
    padding: 9px 0px;
    border: 2px solid black;
    border-radius: 5px;
    font-size: 20px;
}
.calculater{
    text-align: center;
    font-family: cursive;
    font-size: larger;
    color: rgb(83, 172, 0);
   text-decoration: underline;
}
.cal{
   background: black;
border: 5px solid rgb(180, 76, 76);
margin: 0 450px 250px 450px;

}
    </style>
 
</head>
<body>
    
    <div class="calculater">
    <h1><b>This is my calculater &#128131 </b></h1>
    <div class="cal">
    <div class="container">
       
       <div class="row">    
          <input class="input" type="text"/>
      </div> 
   <hr>
    <div class="row">
        <button class="button">c</button>
        <button class="button">&#8592</button>
        <button class="button">&#8730</button>
        <button class="button">/</button>
       </div>
       <div class="row">
        <button class="button">7</button>
        <button class="button">8</button>
        <button class="button">9</button>
        <button class="button">*</button>
       </div>
       <div class="row">
        <button class="button">4</button>
        <button class="button">5</button>
        <button class="button">6</button>
        <button class="button">-</button>
       </div>
       <div class="row">
        <button class="button">1</button>
        <button class="button">2</button>
        <button class="button">3</button>
        <button class="button">+</button>
       </div>
       <div class="row">
        <button class="button">%</button>
        <button class="button">0</button>
        <button class="button">.</button>
        <button class="button">=</button>
       </div>
    
</div>
</div>
    </div>
   
    <!-- <script src="script.js"></script> -->
     <script>
    let string = "";
    let buttons = document.querySelectorAll('.button');
    Array.from(buttons).forEach((button)=>{
      button.addEventListener('click', (e)=>{
        if(e.target.innerHTML == '='){
          string = eval(string);
          document.querySelector('input').value = string;
        }
        else if (e.target.innerHTML == '&#8592' ) {
          string="--e"
          document.querySelector('input').value = string;
         }
          
        else if(e.target.innerHTML == 'c' ){
          string = " "
          document.querySelector('input').value = string;
        }
        
        else{ 
        console.log(e.target)
        string = string + e.target.innerHTML;
        document.querySelector('input').value = string;
          }
         })
    })
</script>
    
</body>
</html>
