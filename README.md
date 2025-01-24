<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Portal</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #007bff;
            color: white;
            padding: 15px;
            text-align: center;
        }
        .container {
            margin: 20px;
            padding: 20px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        button {
            background-color: #007bff;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

<header>
    <h1>User Portal</h1>
</header>

<!-- Login Page -->
<section id="login" class="container">
    <h2>Login</h2>
    <form onsubmit="return validateLogin()">
        <div class="form-group">
            <label for="username">Username</label>
            <input type="text" id="username" name="username" required>
        </div>
        <div class="form-group">
            <label for="password">Password</label>
            <input type="password" id="password" name="password" required>
        </div>
        <button type="submit">Login</button>
    </form>
</section>

<!-- User Information Page -->
<section id="user-info" class="container" style="display: none;">
    <h2>User Information</h2>
    <form>
        <div class="form-group">
            <label for="fullname">Full Name</label>
            <input type="text" id="fullname" name="fullname">
        </div>
        <div class="form-group">
            <label for="email">Email</label>
            <input type="email" id="email" name="email">
        </div>
        <div class="form-group">
            <label for="phone">Phone</label>
            <input type="tel" id="phone" name="phone">
        </div>
        <button type="button" onclick="showProfile()">Next</button>
    </form>
</section>

<!-- Personal Profile Page -->
<section id="profile" class="container" style="display: none;">
    <h2>Personal Profile</h2>
    <p><strong>Full Name:</strong> <span id="profileName"></span></p>
    <p><strong>Email:</strong> <span id="profileEmail"></span></p>
    <p><strong>Phone:</strong> <span id="profilePhone"></span></p>
</section>

<script>
    function validateLogin() {
        const password = document.getElementById('password').value;
        if (password.length < 8) {
            alert('Password must be at least 8 characters long.');
            return false;
        }
        document.getElementById('login').style.display = 'none';
        document.getElementById('user-info').style.display = 'block';
        return false; // Prevent form submission for demonstration
    }

    function showProfile() {
        const name = document.getElementById('fullname').value;
        const email = document.getElementById('email').value;
        const phone = document.getElementById('phone').value;

        document.getElementById('profileName').textContent = name;
        document.getElementById('profileEmail').textContent = email;
        document.getElementById('profilePhone').textContent = phone;

        document.getElementById('user-info').style.display = 'none';
        document.getElementById('profile').style.display = 'block';
    }
</script>

</body>
</html>
