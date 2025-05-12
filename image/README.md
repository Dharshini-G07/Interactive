# Ex.08 Design of Interactive Image Gallery
## Date:12/5/2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :

imsge.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body bgcolor="lightpink">
    <header>
        <h1 align="center">GALLERY</h1>
    </header>
    <div class="gallery">
        <div class="gallery-item" onclick="openModal(this)">
            <img src="bunny.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="dog.jpg"  >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="grey.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="image.png" >
        </div>
        
    </div>

    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="modalImage">
        <div id="caption"></div>
    </div>

    <script src="style.js"></script>
</body>
</html>
```

style.js
```
function openModal(element) {
    const modal = document.getElementById("modal");
    const modalImage = document.getElementById("modalImage");
    const caption = document.getElementById("caption");

    modal.style.display = "flex";
    modalImage.src = element.querySelector("img").src;
    caption.textContent = element.querySelector("img").alt;
}

function closeModal() {
    const modal = document.getElementById("modal");
    modal.style.display = "none";
}
```

style.css
```
.gallery{
    display: flex;
    justify-content: center;
    gap: 40px;
    margin-top: 20px;
}
img{
    width: 250px;
    height: 200px;
    object-fit: cover;
    border-radius: 10px;
}
.modal{
    margin-top: 50px;
    margin-left: 45%;
}
```

## OUTPUT:
![alt text](<Screenshot 2025-05-12 174110.png>)
![alt text](<Screenshot 2025-05-12 174128.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
