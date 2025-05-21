# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨


Answer
@ index.html


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>JavaScript & DOM Practice</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1 id="main-title">Welcome to DOM Manipulation</h1>
  </header>

  <main>
    <section>
      <p id="description">This paragraph will change when the button is clicked.</p>
      <button onclick="changeText()">Change Text</button>
    </section>

    <section>
      <button onclick="changeStyle()">Change Style</button>
    </section>

    <section>
      <button onclick="addElement()">Add Element</button>
      <button onclick="removeElement()">Remove Element</button>
      <div id="dynamic-container"></div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 DOM Learning Project</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

@ script.js

function changeText() {
  const para = document.getElementById("description");
  para.textContent = "The text has been updated using JavaScript!";
}

function changeStyle() {
  const title = document.getElementById("main-title");
  title.style.color = "tomato";
  title.style.fontSize = "2.5rem";
  title.style.textTransform = "uppercase";
}

function addElement() {
  const container = document.getElementById("dynamic-container");
  const newDiv = document.createElement("div");
  newDiv.textContent = "New element added!";
  newDiv.className = "dynamic-box";
  container.appendChild(newDiv);
}

function removeElement() {
  const container = document.getElementById("dynamic-container");
  if (container.lastElementChild) {
    container.removeChild(container.lastElementChild);
  }
}


@style.css (Bonus)

body {
  font-family: Arial, sans-serif;
  padding: 20px;
}

button {
  margin: 10px 5px;
  padding: 10px 15px;
  cursor: pointer;
}

.dynamic-box {
  margin-top: 10px;
  padding: 10px;
  background-color: #f0f0f0;
  border: 1px solid #ccc;
}

