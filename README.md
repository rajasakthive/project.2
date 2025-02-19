<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blood Donation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f9fa;
            text-align: center;
        }
        .container {
            width: 80%;
            margin: auto;
            padding: 20px;
        }
        h1 {
            color: #d9534f;
        }
        .options {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        .option {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            width: 220px;
            text-align: center;
        }
        .option a {
            display: block;
            text-decoration: none;
            color: #d9534f;
            font-weight: bold;
            margin-top: 10px;
        }
        .footer {
            margin-top: 40px;
            padding: 10px;
            background: #d9534f;
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Donate Blood, Save Lives</h1>
        <p>Join us in making a difference. Choose an option below:</p>
        <div class="options">
            <div class="option">
                <h3>Register as Donor</h3>
                <a href="register.html">Sign Up</a>
            </div>
            <div class="option">
                <h3>Find a Blood Bank</h3>
                <a href="bloodbanks.html">Locate</a>
            </div>
            <div class="option">
                <h3>Learn More</h3>
                <a href="learnmore.html">Information</a>
            </div>
            <div class="option">
                <h3>Contact Us</h3>
                <a href="contact.html">Get in Touch</a>
            </div>
            <div class="option">
                <h3>Upcoming Camps</h3>
                <a href="camps.html">View Events</a>
            </div>
            <div class="option">
                <h3>Volunteer</h3>
                <a href="volunteer.html">Join Now</a>
            </div>
        </div>
    </div>
    <div class="footer">
        <p>&copy; 2025 Blood Donation Initiative | All Rights Reserved</p>
    </div>
</body>
</html>

<!-- Register Page -->
<!DOCTYPE html>
<html>
<head>
    <title>Register as Donor</title>
    <script>
        function submitForm(event) {
            event.preventDefault();
            let name = document.getElementById("name").value;
            let bloodType = document.getElementById("bloodType").value;
            let contact = document.getElementById("contact").value;
            
            fetch("http://localhost:5000/register", {
                method: "POST",
                headers: {
                    "Content-Type": "application/json"
                },
                body: JSON.stringify({ name, bloodType, contact })
            })
            .then(response => response.json())
            .then(data => alert("Registration Successful!"))
            .catch(error => console.error("Error:", error));
        }
    </script>
</head>
<body>
    <h2>Register as a Blood Donor</h2>
    <form onsubmit="submitForm(event)">
        <label>Name:</label> <input type="text" id="name"><br>
        <label>Blood Type:</label> <input type="text" id="bloodType"><br>
        <label>Contact:</label> <input type="text" id="contact"><br>
        <button type="submit">Register</button>
    </form>
</body>
</html>

<!-- Contact Page -->
<!DOCTYPE html>
<html>
<head>
    <title>Contact Us</title>
</head>
<body>
    <h2>Contact Us</h2>
    <p>Email: support@blooddonation.com</p>
    <p>Phone: +1234567890</p>
</body>
</html>
        
