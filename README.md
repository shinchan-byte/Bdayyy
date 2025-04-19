<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Zubia!</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1 class="title">Happy Birthday, Zubia!</h1>
        <p class="message">Wishing you a day filled with love, joy, and wonderful surprises!</p>
        <div class="balloons">
            <div class="balloon balloon1"></div>
            <div class="balloon balloon2"></div>
            <div class="balloon balloon3"></div>
            <div class="balloon balloon4"></div>
        </div>
        <button class="wish-button" onclick="showWish()">Click for a Special Wish!</button>
        <div class="wish" id="wish"></div>
    </div>
    <script src="script.js"></script>
</body>
</html>body {
    background-color: #f0e68c; /* Light yellow background */
    font-family: 'Arial', sans-serif; /* Font style */
    overflow: hidden; /* Prevents scrolling */
    margin: 0; /* Removes default margin */
    padding: 0; /* Removes default padding */
}

.container {
    text-align: center; /* Center-aligns text */
    position: relative; /* Allows absolute positioning of balloons */
    padding: 50px; /* Adds padding around the container */
}

.title {
    font-size: 3em; /* Large font size for title */
    color: #ff6f61; /* Coral color */
    animation: fadeIn 2s; /* Fade-in animation */
}

.message {
    font-size: 1.5em; /* Medium font size for message */
    color: #333; /* Dark gray color */
    margin: 20px 0; /* Margin above and below */
    animation: fadeIn 2s 0.5s; /* Fade-in animation with delay */
}

.balloons {
    position: absolute; /* Allows balloons to float above the text */
    bottom: 0; /* Aligns balloons to the bottom */
    left: 50%; /* Centers balloons horizontally */
    transform: translateX(-50%); /* Adjusts for centering */
}

.balloon {
    width: 50px; /* Width of the balloon */
    height: 80px; /* Height of the balloon */
    border-radius: 25px 25px 0 0; /* Rounded top */
    position: relative; /* Allows positioning of the string */
    display: inline-block; /* Displays balloons inline */
    margin: 0 10px; /* Margin between balloons */
    animation: float 3s infinite; /* Floating animation */
}

.balloon1 { background-color: #ff6f61; } /* Coral */
.balloon2 { background-color: #6fa3ff; } /* Light blue */
.balloon3 { background-color: #ffcc5c; } /* Light yellow */
.balloon4 { background-color: #88d8b0; } /* Light green */

.balloon:after {
    content: '';
    width: 10px; /* Width of the string */
    height: 10px; /* Height of the string */
    background-color: #333; /* Dark color for the string */
    border-radius: 50%; /* Round string end */
    position: absolute; /* Positions the string */
    bottom: -10px; /* Positions below the balloon */
    left: 50%; /* Centers the string */
    transform: translateX(-50%); /* Adjusts for centering */
}

.wish-button {
    padding: 10px 20px; /* Padding for button */
    font-size: 1.2em; /* Font size for button */
    background-color: #ff6f61; /* Coral color */
    color: white; /* White text */
    border: none; /* No border */
    border-radius: 5px; /* Rounded corners */
    cursor: pointer; /* Pointer cursor on hover */
    margin-top: 20px; /* Margin above button */
    animation: fadeIn 2s 1s; /* Fade-in animation with delay */
}

.wish {
    margin-top: 20px; /* Margin above wish text */
    font-size: 1.5em; /* Font size for wish */
    color: #333; /* Dark gray color */
    display: none; /* Hidden by default */
}

@keyframes float {
    0% { transform: translateY(0); } /* Start position */
    50% { transform: translateY(-20px); } /* Float up */
    100% { transform: translateY(0); } /* Return to start */
}

@keyframes fadeIn {
    from { opacity: 0; } /* Start invisible */
    to { opacity: 1; } /* End visible */
}function showWish() {
    const wishElement = document.getElementById('wish');
    wishElement.innerHTML = "May all your dreams come true! 🎉";
    wishElement.style.display = "block";
    wishElement.style.animation = "fadeIn 2s";
}
