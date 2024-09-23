<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Text Writer Effect</title>
    <style>
        #animated-text {
            font-size: 2.5em;
            text-align: center;
            white-space: nowrap;
            overflow: hidden; /* Ensures the text doesn't wrap */
            border-right: 4px solid; /* Cursor effect */
            width: 0; /* Start with 0 width */
            animation: typing 4s steps(30, end) forwards, blink-caret 0.75s step-end infinite;
        }

        @keyframes typing {
            from { width: 0; }
            to { width: 23em; } /* Adjust to the length of your text */
        }

        @keyframes blink-caret {
            from, to { border-color: transparent; }
            50% { border-color: black; } /* Change to match your text color */
        }
    </style>
</head>
<body>

    <h1 id="animated-text"></h1>
    <h3 align="center">A passionate frontend developer from India</h3>

    <h3 align="left">Connect with me:</h3>
    <p align="left">
        <a href="https://linkedin.com/in/yourprofile" target="_blank">LinkedIn</a> | 
        <a href="https://github.com/yourusername" target="_blank">GitHub</a> | 
        <a href="https://twitter.com/yourusername" target="_blank">Twitter</a>
    </p>

    <script>
        const text = "Hi 👋, I'm Omniscient";
        let index = 0;

        function type() {
            if (index < text.length) {
                document.getElementById("animated-text").innerHTML += text.charAt(index);
                index++;
                setTimeout(type, 100); // Adjust typing speed here
            }
        }

        window.onload = type; // Start typing when the page loads
    </script>

</body>
</html>
