<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript DOM Manipulation</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>Welcome to JavaScript and DOM Manipulation</h1>
    </header>

    <main>
        <section>
            <p id="textContent">This text will change dynamically when the button is clicked.</p>
        </section>

        <button id="changeTextButton">Change Text Content</button>
        <button id="changeStyleButton">Change Background Color</button>
        <button id="addElementButton">Add New Element</button>
    </main>

    <footer>
        <p>Created by Your Name</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
/* style.css */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 20px;
}

header {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 10px;
}

footer {
    text-align: center;
    padding: 10px;
    background-color: #4CAF50;
    color: white;
}

button {
    margin: 10px;
    padding: 10px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}
// script.js

// Change text content dynamically
document.getElementById('changeTextButton').addEventListener('click', function() {
    document.getElementById('textContent').textContent = 'The text content has been changed!';
});

// Change background color dynamically
document.getElementById('changeStyleButton').addEventListener('click', function() {
    document.body.style.backgroundColor = '#ADD8E6';  // Light blue color
});

// Add a new element dynamically
document.getElementById('addElementButton').addEventListener('click', function() {
    let newElement = document.createElement('p');
    newElement.textContent = 'A new paragraph has been added dynamically!';
    document.body.appendChild(newElement);
});
