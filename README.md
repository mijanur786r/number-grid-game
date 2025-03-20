<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Number Grid App</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        .number-button {
            width: 3rem;
            height: 3rem;
        }
    </style>
</head>
<body class="bg-gray-100 flex items-center justify-center min-h-screen">
    <div class="bg-white p-6 rounded-lg shadow-lg">
        <div id="number-grid" class="grid grid-cols-5 gap-2">
            <button class="number-button bg-black text-white rounded">1</button>
            <button class="number-button bg-black text-white rounded">2</button>
            <button class="number-button bg-black text-white rounded">3</button>
            <button class="number-button bg-black text-white rounded">4</button>
            <button class="number-button bg-black text-white rounded">5</button>
            <button class="number-button bg-black text-white rounded">6</button>
            <button class="number-button bg-black text-white rounded">7</button>
            <button class="number-button bg-black text-white rounded">8</button>
            <button class="number-button bg-black text-white rounded">9</button>
            <button class="number-button bg-black text-white rounded">10</button>
            <button class="number-button bg-black text-white rounded">11</button>
            <button class="number-button bg-black text-white rounded">12</button>
            <button class="number-button bg-black text-white rounded">13</button>
            <button class="number-button bg-black text-white rounded">14</button>
            <button class="number-button bg-black text-white rounded">15</button>
            <button class="number-button bg-black text-white rounded">16</button>
            <button class="number-button bg-black text-white rounded">17</button>
            <button class="number-button bg-black text-white rounded">18</button>
            <button class="number-button bg-black text-white rounded">19</button>
            <button class="number-button bg-black text-white rounded">20</button>
            <button class="number-button bg-black text-white rounded">21</button>
            <button class="number-button bg-black text-white rounded">22</button>
            <button class="number-button bg-black text-white rounded">23</button>
            <button class="number-button bg-black text-white rounded">24</button>
            <button class="number-button bg-black text-white rounded">25</button>
        </div>
        <div class="mt-4 flex justify-center">
            <button id="start-button" class="bg-blue-500 text-white px-4 py-2 rounded">Start</button>
        </div>
    </div>

    <script>
        document.getElementById('start-button').addEventListener('click', function() {
            // Reset all buttons to black
            const buttons = document.querySelectorAll('.number-button');
            buttons.forEach(button => {
                button.classList.remove('bg-red-500');
                button.classList.add('bg-black');
            });

            // Generate 5 unique random numbers
            const randomNumbers = [];
            while (randomNumbers.length < 5) {
                const randomNumber = Math.floor(Math.random() * 25) + 1;
                if (!randomNumbers.includes(randomNumber)) {
                    randomNumbers.push(randomNumber);
                }
            }

            // Set the selected buttons to red
            randomNumbers.forEach(number => {
                const button = buttons[number - 1];
                button.classList.remove('bg-black');
                button.classList.add('bg-red-500');
            });

            // Display the random numbers
            alert("Random Red Numbers: " + randomNumbers.join(", "));
        });
    </script>
</body>
</html>
