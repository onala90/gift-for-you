<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>African Woman's Heart</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            text-align: center;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .heart {
            position: relative;
            width: 200px;
            height: 200px;
            margin: 0 auto;
        }
        .heart:before,
        .heart:after {
            content: "";
            position: absolute;
            width: 100px;
            height: 150px;
            background: red;
            border-radius: 100px 100px 0 0;
            top: 0;
            left: 50px;
        }
        .heart:before {
            transform: rotate(-45deg);
            left: 0;
        }
        .heart:after {
            transform: rotate(45deg);
            right: 0;
        }
        .name {
            cursor: pointer;
            margin: 10px 0;
            font-weight: bold;
        }
        .hidden {
            display: none;
        }
        .message {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>An African Woman's Heart</h1>
        <div class="heart">
            <div class="name" onclick="askQuestion('John')">John</div>
            <div class="name" onclick="askQuestion('Mary')">Mary</div>
            <div class="name" onclick="askQuestion('Alex')">Alex</div>
        </div>
        <div id="question" class="hidden">
            <p id="questionText"></p>
            <input type="text" id="answer" placeholder="Your answer here">
            <button onclick="checkAnswer()">Submit</button>
        </div>
        <div id="message" class="message hidden"></div>
    </div>

    <script>
        const questions = {
            John: { question: "What is 2 + 2?", answer: "4", message: "Hello John! Your message is: Welcome!" },
            Mary: { question: "What is the capital of France?", answer: "Paris", message: "Hello Mary! Your message is: Bonjour!" },
            Alex: { question: "What is the color of the sky?", answer: "Blue", message: "Hello Alex! Your message is: Stay positive!" }
        };

        let currentName = '';

        function askQuestion(name) {
            currentName = name;
            const question = questions[name].question;
            document.getElementById('questionText').innerText = question;
            document.getElementById('question').classList.remove('hidden');
        }

        function checkAnswer() {
            const userAnswer = document.getElementById('answer').value.trim();
            if (userAnswer.toLowerCase() === questions[currentName].answer.toLowerCase()) {
                document.getElementById('message').innerText = questions[currentName].message;
                document.getElementById('message').classList.remove('hidden');
                document.getElementById('question').classList.add('hidden');
            } else {
                alert('Incorrect answer, please try again.');
            }
        }
    </script>
</body>
</html>
