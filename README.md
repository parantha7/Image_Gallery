# Ex.08 Design of Interactive Image Gallery
# Name  : PARANTHAMAN S 
# Reg No: 212224040232
## DATE: 19-05-2025
## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
~~~
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Toyota Showcase</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Montserrat', sans-serif;
      background: linear-gradient(to right, #000000, #434343);
      color: #fff;
    }

    header {
      text-align: center;
      padding: 40px 20px 20px;
    }

    header h1 {
      font-size: 3rem;
      color: #ff4d00;
      margin-bottom: 10px;
      text-shadow: 2px 2px 8px #000;
    }

    header p {
      font-size: 1.2rem;
      color: #ccc;
    }

    .gallery-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      padding: 40px;
      max-width: 1200px;
      margin: auto;
    }

    .gallery-item {
      position: relative;
      overflow: hidden;
      border-radius: 15px;
      cursor: pointer;
      transition: transform 0.4s ease;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.6);
    }

    .gallery-item:hover {
      transform: scale(1.05);
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: opacity 0.3s ease;
    }

    .caption {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      padding: 15px;
      background: rgba(0, 0, 0, 0.6);
      font-size: 1.2rem;
      font-weight: bold;
      color: #ff4d00;
      text-align: center;
      letter-spacing: 1px;
    }

    #lightbox {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.95);
      justify-content: center;
      align-items: center;
      z-index: 9999;
    }

    #lightboxContent {
      text-align: center;
      max-width: 90%;
      max-height: 80%;
    }

    #lightboxImage {
      max-width: 100%;
      max-height: 80vh;
      border-radius: 10px;
      border: 3px solid #ff4d00;
      box-shadow: 0 0 20px #ff4d00;
    }

    .close-button {
      margin-top: 20px;
      padding: 10px 20px;
      font-size: 1rem;
      background: #e60000;
      border: none;
      border-radius: 8px;
      color: white;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    .close-button:hover {
      background: #cc0000;
    }

    footer {
      text-align: center;
      padding: 20px;
      background-color: #111;
      color: #aaa;
      font-size: 14px;
      border-top: 1px solid #333;
    }
  </style>
  <script>
    function displayLightbox(src, alt) {
      document.getElementById("lightboxImage").src = src;
      document.getElementById("lightboxImage").alt = alt;
      document.getElementById("lightbox").style.display = "flex";
    }

    function hideLightbox() {
      document.getElementById("lightbox").style.display = "none";
    }
  </script>
</head>
<body>

  <header>
    <h1>TOYOTA SHOWCASE</h1>
    <p>Discover the power of the LC 300, Supra, and Hilux</p>
  </header>

  <div class="gallery-container">
    <div class="gallery-item" onclick="displayLightbox('toyota-lc300.jpg', 'Toyota Land Cruiser 300')">
      <img src="lc.jpeg" alt="Toyota Land Cruiser 300">
      <div class="caption">Toyota LC 300</div>
    </div>
    <div class="gallery-item" onclick="displayLightbox('toyota-supra.jpg', 'Toyota Supra')">
      <img src="sup.jpeg" alt="Toyota Supra">
      <div class="caption">Toyota Supra</div>
    </div>
    <div class="gallery-item" onclick="displayLightbox('toyota-hilux.jpg', 'Toyota Hilux')">
      <img src="hel.jpg" alt="Toyota Hilux">
      <div class="caption">Toyota Hilux</div>
    </div>
  </div>

  <div id="lightbox">
    <div id="lightboxContent">
      <img id="lightboxImage" src="" alt="">
      <br>
      <button class="close-button" onclick="hideLightbox()">Close</button>
    </div>
  </div>

  <footer>
    Designed & Developed by paranthaman s
  </footer>

</body>
</html>

~~~

## OUTPUT
![alt text](image.png)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
