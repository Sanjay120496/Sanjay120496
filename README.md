!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bright Byte</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome to Bright Byte</h1>
    </header>
    <main>
        <section>
            <h2>Enter Your Name</h2>
            <input type="text" id="nameInput" placeholder="Enter your name">
            <button onclick="submitName()">Submit</button>
        </section>
    </main>
    <script src="script.js"></script>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #f0f0f0;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
}

input[type="text"] {
    padding: 10px;
    width: 200px;
    margin-right: 10px;
}

button {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}
function submitName() {
    var name = document.getElementById("nameInput").value;
    if (name.trim() !== "") {
        localStorage.setItem("username", name);
        window.location.href = "language.html";
    } else {
        alert("Please enter your name.");
    }

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Language Selection</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome, <span id="username"></span>!</h1>
    </header>
    <main>
        <section>
            <h2>Select a Language to Learn</h2>
            <ul>
                <!-- List of 22 languages here -->
                <!-- Each language should link to a page with word translations -->
            </ul>
        </section>
    </main>
    <script src="script.js"></script>
    <script>
        var username = localStorage.getItem("username");
        if (username) {
            document.getElementById("username").textContent = username;
        }
    </script>
</body>
</html>
