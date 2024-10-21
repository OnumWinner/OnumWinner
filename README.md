git clone https://github.com/yourusername/yourusername.github.io.git
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Development Masterclass</title>
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
            line-height: 1.6;
        }
        header {
            background-color: #1e90ff;
            color: white;
            text-align: center;
            padding: 20px 0;
        }
        #animated-heading {
            font-size: 2em;
            font-weight: 600;
        }
        p {
            padding: 0 20px;
        }
        h2 {
            font-size: 1.5em;
            color: #1e90ff;
            text-align: center;
            margin-top: 20px;
        }
        ul {
            list-style-type: square;
            padding: 0 20px;
        }
        #payment {
            margin-top: 20px;
            text-align: center;
        }
        #payment-btn {
            padding: 10px 20px;
            background-color: #28a745;
            color: white;
            border: none;
            cursor: pointer;
            font-size: 1.2em;
        }
        #payment-btn:disabled {
            background-color: #ccc;
            cursor: not-allowed;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
        }
        .warning {
            color: red;
            font-weight: bold;
            text-align: center;
            padding-top: 10px;
        }
        /* Animation */
        @keyframes slide-in {
            0% {
                left: -100%;
            }
            100% {
                left: 0;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1 id="animated-heading">KING. LEARN WEB DESIGN AND DEVELOPMENT WITH GRAPHICS DESIGN FOR MORE THAN HALF THE PRICE.</h1>
        <p>With the evolution of technology and skills acquisition, the world has always been a global village, and technological innovations have come to stay. Become a tech bro or sis in 2 months and get ready to dive into the world of technology by the end of this innovative class. As you simultaneously complete a 2 months long journey to Web development and Graphics designing, you can either become a full stack developer, a UI/UX designer, or even a resource person like me, YourKing :)</p>
        <p>Awoof has never been better, don't miss this opportunity!</p>
        <h2>Requirements:</h2>
        <ul>
            <li>Your Phone/Laptop</li>
            <li>1 hour 30 minutes daily</li>
            <li>Zeal to learn</li>
        </ul>
        <p class="warning"><strong>Note:</strong> Limited to 20 participants. Sign up now!</p>
    </header>

    <section id="payment">
        <h2>Payment Method</h2>
        <p>Pay via Bank Transfer:</p>
        <button id="payment-btn">Pay Now</button>
    </section>

    <section id="teachers">
        <h2>Meet the Teachers</h2>
        <p>ONUM, WINNER - ABSU (Host)</p>
        <p>ANYA, SARAH - PORT HARCOURT (Graphics Designer)</p>
        <p>CHIDI - MOUAU (Full Stack Developer)</p>
    </section>

    <footer>
        <p>&copy; 2024 Web Development & Graphics Design Masterclass. All rights reserved.</p>
    </footer>

    <script>
        // Sliding Animation for the Heading
        document.addEventListener("DOMContentLoaded", function() {
            const heading = document.getElementById('animated-heading');
            heading.style.position = 'relative';
            heading.style.animation = 'slide-in 3s ease-out forwards';
        });

        // Dialog box for Full Name (prompt) and confirm
        window.onload = function() {
            const fullName = prompt("Please enter your Full Name:");
            if (fullName) {
                const confirmation = confirm("Would you like to take your tech skills to the next level?");
                if (confirmation) {
                    alert(`Welcome ${fullName}! You're on your way to mastering tech skills.`);
                } else {
                    alert("Maybe next time! But don’t miss this opportunity.");
                }
            }
        };

        // Initialize the number of signups
        let signupCount = 0;

        // Get the signup button element
        const signupBtn = document.getElementById('payment-btn');

        // Add event listener to the signup button
        signupBtn.addEventListener('click', function() {
            // Increment the signup count on each click
            signupCount++;

            // Check if the signup count is less than or equal to 20
            if (signupCount <= 20) {
                alert(`Thank you for signing up! There are now ${20 - signupCount} slots remaining.`);
            } else {
                // Disable the signup button and notify the user
                signupBtn.disabled = true;
                alert("Signups are now closed! We have reached the limit of 20 participants.");
            }
        });
    </script>

</body>
</html>
git add .
git commit -m "Initial website"
git push origin main