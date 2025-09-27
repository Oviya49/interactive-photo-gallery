##  INTERACTIVE-PHOTO-GALLERY

## PROGRAM:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Photo Gallery</title>
  <style>
    body { font-family: Arial, sans-serif; text-align: center; margin: 20px; }
    img { width: 200px; margin: 10px; border: 2px solid #ccc; border-radius: 8px; cursor: pointer; }
    img:focus { outline: 3px solid blue; }
  </style>
</head>
<body>
  <h1>My Interactive Photo Gallery</h1>
  <div id="gallery">
    <img src="img1.jpg" alt="Beautiful Sunset" tabindex="0">
    <img src="img2.jpg" alt="Snowy Mountains" tabindex="0">
    <img src="img3.jpg" alt="Calm Ocean" tabindex="0">
    <img src="img4.jpg" alt="City Skyline" tabindex="0">
    <img src="img5.jpg" alt="Green Forest" tabindex="0">
    <img src="img6.jpg" alt="Desert Dunes" tabindex="0">
  </div>

  <script>
    window.onload = addTabFocus;
    function addTabFocus() {
      console.log("Page loaded and tab focus added");
      var images = document.querySelectorAll("#gallery img");
      for (var i = 0; i < images.length; i++) {
        images[i].addEventListener("mouseover", function() {
          this.style.border = "2px solid red";
        });
        images[i].addEventListener("mouseleave", function() {
          this.style.border = "2px solid #ccc";
        });
        images[i].addEventListener("focus", function() {
          this.style.border = "2px solid green";
          console.log("Image focused");
        });
        images[i].addEventListener("blur", function() {
          this.style.border = "2px solid #ccc";
          console.log("Image blurred");
        });
      }
    }
  </script>
</body>
</html>

```
## OUTPUT:
<img width="1918" height="1024" alt="image" src="https://github.com/user-attachments/assets/94c36405-87b2-45ea-a203-2f31f01ec7d3" />
