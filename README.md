@page
@model IndexModel
@{
    ViewData["Title"] = "SSB Ghassa Gang Home";
}

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>@ViewData["Title"]</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f2f2f2;
        }

        header {
            background-color: #004080;
            color: white;
            padding: 15px;
            text-align: center;
        }

        nav {
            background-color: #333;
            overflow: hidden;
        }

        nav a {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 20px;
            text-decoration: none;
        }

        nav a:hover {
            background-color: #ddd;
            color: black;
        }

        .container {
            position: relative; /* Ensure container is positioned relative */
            max-width: 800px; /* Adjust container width */
            margin: auto; /* Center container horizontally */
            padding: 20px;
            text-align: center; /* Center align the content */
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        .photo {
            width: 100%;
            max-width: 600px;
            display: block;
            margin: 20px auto;
        }

        .message {
            position: absolute; /* Position the message absolutely */
            top: 10px; /* Adjust top position */
            right: 10px; /* Adjust right position */
            background-color: red; /* Red background */
            color: black; /* Black text */
            padding: 10px; /* Padding around the text */
            z-index: 1; /* Ensure message is above other content */
        }

        video {
            width: 100%; /* Set video width to 100% of its container */
            max-width: 600px; /* Limit maximum width for larger screens */
            display: block; /* Ensure video is displayed as a block element */
            margin: 20px auto; /* Center the video horizontally */
        }
    </style>
</head>
<body>
    <header>
        <h1>SSB - Sashastra Seema Bal</h1>
    </header>
    <nav>
        <a asp-page="/Index">Home</a>
        <a asp-page="/About">About Us</a>
        <a asp-page="/Services">Services</a>
        <a asp-page="/Contact">Contact</a>
    </nav>
    <div class="container">
        <h2>Welcome to SSB</h2>
        <p>This is a homepage for Ghassa Gang of Sashastra Seema Bal.</p>
        <img src="~/images/pawar.jpeg" alt="Photo" class="photo">
        <p class="message">Message from the Ghassa Gang: All members are hereby requested to bring their own golgappa, whereas daru will be provided by the one whose turn it is.</p>
        <h3>Watch Our Ghassa Gang Video</h3>
        <video controls>
            <source src="~/videos/video.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
    <footer>
        <p>&copy; 2024 Sashastra Seema Bal. All rights reserved.</p>
    </footer>
</body>
</html>
