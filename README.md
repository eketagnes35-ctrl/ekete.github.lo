<!DOCTYPE html>
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
            position: absolute;
            top: 120px;
            left: 80px;
            width: 240px;
            display: none;
            opacity: 0.8;
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

<img id="shirt" class="outfit" src="https://i.imgur.com/7Q7Z8wB.png">

<img id="dress" class="outfit" src="https://i.imgur.com/3ZQ3Z3M.png">

<img id="jacket" class="outfit" src="https://i.imgur.com/5Q9V7fK.png">

</div>


<h2>Select Outfit</h2>

<div class="choices">

<img src="https://i.imgur.com/7Q7Z8wB.png" onclick="showOutfit('shirt')">

<img src="https://i.imgur.com/3ZQ3Z3M.png" onclick="showOutfit('dress')">

<img src="https://i.imgur.com/5Q9V7fK.png" onclick="showOutfit('jacket')">

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