<!DOCTYPE html>
<html>
<head>
    <title>Sera</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <div class="container">
        <img src="Yiee.gif" alt="Thank you GIF" width="300">
        <h1>Hi Crush</h1>
        <h2>Gusto kita,Can I court You?</h2>
        <div class="buttons">
            <button id="no-btn">No</button>
            <button id="yes-btn">Yes</button>
        </div>
        <div class="popup" id="popup">
            <p>
                <img src="kiss.gif" alt="Thank you GIF" width="200">
            </p>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
<style>
body {
    font-family: 'Great Vibes', cursive;
    text-align: center;
    margin: 0;
    background-color:black;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh; /* Ensure the body takes up full height */
}
p {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 10vh; /* Adjust height based on the container */
}
.container {
    padding: 30px;
}

h1,h2{
    font-size: 36px;
    margin-bottom: 30px;
    color: #e91e63;
}

.buttons {
    margin: 20px;
}

button {
    font-size: 20px;
    padding: 12px 24px;
    margin: 10px;
    border: none;
    border-radius: 20px;
    background-color: #ff4081;
    color: #fff;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #ff5c8d;
}

.popup {
    display: none;
    background-color: #fff;
    border: 1px solid #e91e63;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    padding: 20px;
    position: fixed; /* Use fixed to prevent scrolling issues */
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 999;
    font-family: 'Dancing Script', cursive;
    font-size: 24px;
    color: #e91e63;
}

/* Add a smooth fade-in animation for the popup */
.popup.fade-in {
    animation: fadeIn 0.3s ease;
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

</style>
<script>
    const noButton = document.getElementById("no-btn");
const yesButton = document.getElementById("yes-btn");
const popup = document.getElementById("popup");

noButton.addEventListener("mouseover", () => {
    noButton.style.position = "absolute";
    noButton.style.left = Math.random() * 80 + "vw";
    noButton.style.top = Math.random() * 80 + "vh";
});

yesButton.addEventListener("click", () => {
    popup.style.display = "block";
});

popup.addEventListener("click", () => {
    popup.style.display = "none";
});

// Hide the popup initially
popup.style.display = "none";

</script>
