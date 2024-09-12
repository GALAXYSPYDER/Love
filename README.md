<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I Love You</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            overflow: hidden;
            font-family: Arial, sans-serif;
        }
        .message {
            font-size: 3em;
            color: #fff;
            text-align: center;
            animation: bounce 2s infinite;
        }
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-30px);
            }
            60% {
                transform: translateY(-15px);
            }
        }
        .question {
            display: none;
            font-size: 2em;
            text-align: center;
            margin-top: 20px;
        }
        .option {
            display: inline-block;
            margin: 10px;
            padding: 10px 20px;
            font-size: 1.5em;
            color: #fff;
            background: #007bff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s;
        }
        .option:hover {
            background: #0056b3;
        }
        .no-option {
            position: relative;
        }
        .move {
            animation: move 1s infinite alternate;
        }
        @keyframes move {
            0% { transform: translateX(0) translateY(0); }
            100% { transform: translateX(30px) translateY(-20px); }
        }
    </style>
</head>
<body>
    <div class="message">I love you ❤️ Sneha😽</div>
    <div class="question">
        <div id="yes" class="option">Yes</div>
        <div id="no" class="option no-option">No</div>
    </div>

    <script>
        window.onload = function() {
            setTimeout(() => {
                document.querySelector('.message').style.display = 'none';
                document.querySelector('.question').style.display = 'block';
            }, 5000);

            document.getElementById('no').addEventListener('click', function() {
                this.classList.add('move');
            });

            document.getElementById('yes').addEventListener('click', function() {
                alert('Thank you for loving me!');
            });
        }
    </script>
</body>
</html>
