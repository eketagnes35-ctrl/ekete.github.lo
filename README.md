<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Affiliate Advertisement</title>

<style>
body{
    font-family:Arial, sans-serif;
    background:#f4f4f4;
}

.ad-container{
    width:320px;
    margin:40px auto;
    padding:15px;
    background:white;
    border-radius:10px;
    text-align:center;
    box-shadow:0 5px 15px rgba(0,0,0,.15);
}

.ad-title{
    font-size:20px;
    color:#333;
    margin-bottom:10px;
}

.ad-box{
    width:300px;
    height:250px;
    background:#eee;
    display:flex;
    justify-content:center;
    align-items:center;
    margin:auto;
    border:2px dashed #999;
    color:#777;
}

.ad-note{
    margin-top:15px;
    font-size:14px;
    color:#555;
}
</style>

</head>
<body>

<div class="ad-container">

<h2 class="ad-title">Sponsored Advertisement</h2>

<div class="ad-box">

<!-- Replace this with your affiliate ad code -->

<p>Your Affiliate Ad Appears Here</p>

</div>

<p class="ad-note">
By interacting with this advertisement, you help support our website.
</p>

</div>

</body>
</html><!DOCTYPE html>
<html>
<head>
    <title>Virtual Try-On Demo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f4f4f4;
            text-align: center;
        }

        h1 {
            color: #333;
        }

        .container {
            width: 800px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 15px;
        }

        .tryon-area {
            position: relative;
            width: 400px;
            height: 500px;
            margin: 20px auto;
            border: 2px solid #ccc;
            overflow: hidden;
        }

        #userImage {
            width: 100%;
            height: 100%;
            object-fit: contain;
        } 
.outfit {
    position:absolute;
    top:80px;
    left:50%;
    transform:translateX(-50%);
    width:250px;
    display:none;
    pointer-events:none;
}

        .choices img {
            width: 100px;
            height: 120px;
            object-fit: contain;
            border: 2px solid transparent;
            cursor: pointer;
            margin: 10px;
        }

        .choices img:hover {
            border: 2px solid black;
        }

        input {
            margin: 20px;
        }
    </style>
</head>

<body>

<div class="container">

<h1>Virtual Try-On Fashion Store</h1>

<p>Upload your photo:</p>

<input type="file" accept="image/*" onchange="loadImage(event)">


<div class="tryon-area">

<img id="userImage">

<img id="shirt" class="outfit" src="images/shirt.png">

<img id="dress" class="outfit" src="images/dress.png">

<img id="jacket" class="outfit" src="images/jacket.png">

</div>


<h2>Select Outfit</h2>

<div class="choices">

<img src="images/shirt.png" onclick="showOutfit('shirt')">

<img src="images/dress.png" onclick="showOutfit('dress')">

<img src="images/jacket.png" onclick="showOutfit('jacket')">

</div>


</div>


<script>

function loadImage(event){

    let image = document.getElementById("userImage");

    image.src = URL.createObjectURL(event.target.files[0]);

}


function showOutfit(id){

    document.querySelectorAll(".outfit").forEach(function(item){
        item.style.display="none";
    });

    document.getElementById(id).style.display="block";

}

</script>


</body>
</html>
<!DOCTYPE html>
<html>
<head>

<title>AI Virtual Try-On Fashion Store</title>

<style>

body{
    font-family: Arial;
    background:#111;
    color:white;
    margin:0;
}

header{
    background:#222;
    padding:20px;
    text-align:center;
}

.container{
    padding:30px;
}

.card{
    background:#222;
    padding:20px;
    border-radius:15px;
    margin:20px;
}

button{
    padding:10px 20px;
    background:#ff4d6d;
    color:white;
    border:none;
    border-radius:8px;
    cursor:pointer;
}

select{
    padding:8px;
    margin:5px;
}


.try-area{

position:relative;
width:400px;
height:500px;
background:#333;
margin:auto;
overflow:hidden;

}


#person{

width:100%;
height:100%;
object-fit:contain;

}


#clothes{

position:absolute;
width:200px;
top:120px;
left:100px;
cursor:move;

}


.catalog{

display:flex;
gap:20px;
flex-wrap:wrap;

}


.product{

background:#333;
padding:15px;
border-radius:10px;
width:200px;

}


.product img{

width:100%;

}


.cart{

background:#222;
padding:20px;
margin-top:20px;

}


.ai-box{

background:#444;
padding:30px;
text-align:center;
border-radius:15px;

}


</style>

</head>


<body>


<header>

<h1>AI Virtual Try-On Fashion Store</h1>

</header>



<div class="container">



<div class="card">


<h2>1. Upload Your Photo</h2>


<input type="file" accept="image/*" onchange="upload(event)">



<div class="try-area">


<img id="person">


<img id="clothes" src="images/shirt.png">


</div>


<br>


<button onclick="makeBigger()">Increase Size</button>

<button onclick="makeSmaller()">Decrease Size</button>


</div>




<div class="card">


<h2>2. Choose Outfit</h2>


<div class="catalog">


<div class="product">

<img src="images/shirt.png">

<h3>Classic Shirt</h3>

<p>$35</p>


<select>

<option>Small</option>
<option>Medium</option>
<option>Large</option>

</select>


<select>

<option>Black</option>
<option>White</option>
<option>Blue</option>

</select>


<br><br>

<button onclick="addCart('Classic Shirt','$35')">

Add To Cart

</button>


</div>




<div class="product">


<img src="images/dress.png">


<h3>Summer Dress</h3>

<p>$60</p>


<select>

<option>Small</option>
<option>Medium</option>
<option>Large</option>

</select>


<select>

<option>Red</option>
<option>Pink</option>
<option>Blue</option>

</select>


<br><br>


<button onclick="addCart('Summer Dress','$60')">

Add To Cart

</button>


</div>


</div>


</div>




<div class="cart">


<h2>Shopping Cart</h2>

<ul id="cart"></ul>


</div>





<div class="ai-box">


<h2>AI Try-On Preview</h2>


<p>

This section will connect to an AI clothing model in the future.

</p>


<button onclick="alert('AI model coming soon!')">

Generate AI Try-On

</button>


</div>



</div>




<script>


function upload(event){

let img=document.getElementById("person");

img.src=URL.createObjectURL(event.target.files[0]);

}



// Drag outfit

let outfit=document.getElementById("clothes");


outfit.onmousedown=function(e){

let x=e.clientX-outfit.offsetLeft;
let y=e.clientY-outfit.offsetTop;


document.onmousemove=function(e){

outfit.style.left=e.clientX-x+"px";
outfit.style.top=e.clientY-y+"px";


}


document.onmouseup=function(){

document.onmousemove=null;

}


}




// Resize controls

let size=200;


function makeBigger(){

size+=20;

outfit.style.width=size+"px";

}


function makeSmaller(){

size-=20;

outfit.style.width=size+"px";

}




// Cart


function addCart(name,price){


let item=document.createElement("li");

item.innerHTML=name+" - "+price;


document.getElementById("cart").appendChild(item);


}



</script>


</body>

</html>