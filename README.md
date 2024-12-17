# Ex.08 Design of Interactive Image Gallery
## Date:17-12-2024

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
```
index.html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link
        href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto:wght@300;400;500&family=Gloock&display=swap"
        rel="stylesheet">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Audiowide|Sofia|Trirong">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link
        href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400..700&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap"
        rel="stylesheet">
    <link
        href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400..700&family=Montserrat:ital,wght@0,100;1,100&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap"
        rel="stylesheet">
    <link
        href="https://fonts.googleapis.com/css2?family=Alumni+Sans+Pinstripe:ital@0;1&family=Dancing+Script:wght@400..700&family=Montserrat:ital,wght@0,100;1,100&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap"
        rel="stylesheet">

    <title>Image Gallery</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        h1 {
            padding-top: 5px;
            padding-bottom: 5px;
            color: black;
            font-weight: 900;
            background-image: linear-gradient(to left, rgb(90, 84, 84), whitesmoke);
            font-family: Montserrat;
            font-size: 40px;
            font-weight: bolder;
            font-variant: small-caps;
            text-align: center;
            
        }

        .container {

            margin-top: 4%;
            margin-left: 10%;
            display: flex;
            flex-wrap: wrap;
        }

        .one {
            cursor: pointer;
            transform: scale(1.02);
            margin-bottom: 10%;
            border-radius: 10px;
            margin-left: 100px;
            width: auto;
            height: 300px;
        }
        
        .one:hover {
            transform: scale(1.05);
        }

        .modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background-color: rgba(0, 0, 0, 0.8);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            visibility: hidden;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .modal.visible {
            
            visibility: visible;
            opacity: 1;
        }

        .modal-image {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
        }

        .close-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            padding: 10px 20px;
            font-size: 16px;
            color: #fff;
            background: rgba(0, 0, 0, 0.5);
            border: none;
            cursor: pointer;
            border-radius: 5px;
            transition: background 0.2s ease;
        }

        .close-btn:hover {
            background: rgba(255, 255, 255, 0.2);
        }

        footer {
            margin-top: 70px;
            padding: 5px;
            font-weight: bold;
            font-size: 20px;
            font-family: Montserrat;
            text-align: center;
            background-image: linear-gradient(to left, rgb(90, 84, 84), whitesmoke);
        }
        span{
            color: rgb(0, 109, 109) ;
            

        }
        .tt{
            font-weight: 500;
            color: black;
            font-family: Trirong;
        }
    </style>


</head>

<body>
    <h1>
        <span class="tt">I</span>mage <span class="tt">G</span>allery
    </h1>
    <div class="container">

        <div>
            <img src="founder.jpeg" class="one">
        </div>
        <div>
            <img src="joe.jpeg" alt="" class="one">
        </div>
        <div>
            <img src="robert.jpeg" alt="" class="one">
        </div>
        <div>
            <img src="cilian murphy.jpeg" alt="" class="one">
        </div>

        <div>
            <img src="anne.jpeg" alt="" class="one" >
        </div>
        <div>
            <img src="emma.jpeg" alt="" class="one">
        </div>
        <div>
            <img src="robbi2.jpeg" alt="" class="one">
        </div>
        <div>
            <img src="emilia.jpg" alt="" class="one">
        </div>
    </div>
    <div class="modal">
        <img src="" alt="" class="modal-image">
        <button class="close-btn">X</button>
    </div>


    <footer>
        <p>Designed and Developed by <span>Elavarasan M</span></p>
    </footer>

    <script>
        const modal = document.querySelector('.modal');
        const modalImage = document.querySelector('.modal-image');
        const closeButton = document.querySelector('.close-btn');
        const images = document.querySelectorAll('.one');

        images.forEach((image) => {
            image.addEventListener('click', () => {
                modalImage.src = image.src;
                modal.classList.add('visible'); 
            });
        });

        closeButton.addEventListener('click', () => {
            modal.classList.remove('visible'); 
        });

        modal.addEventListener('click', (e) => {
            if (e.target === modal) {
                modal.classList.remove('visible'); 
            }
        });
    </script>
</body>

</html>
```
## OUTPUT:
![alt text](<Screenshot (120).png>)
![alt text](<Screenshot (121).png>)
![alt text](<Screenshot (122).png>)
![alt text](<Screenshot (123).png>)
![alt text](<Screenshot (124).png>)
![alt text](<Screenshot (125).png>)
![alt text](<Screenshot (126).png>)
![alt text](<Screenshot (127).png>)
![alt text](<Screenshot (128).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
