<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First PHP Page</title>
</head>
<body>
    <h1>Welcome to My First PHP Page</h1>
    <?php
    // Define a variable
    $greeting = "Hello, World!";
    
    // Output the variable
    echo "<p>$greeting</p>";
    
    // Display the current date and time
    echo "<p>Current Date and Time: " . date("Y-m-d H:i:s") . "</p>";
    ?>
    
    <!-- HTML Form to get user input -->
    <form method="post" action="">
        <label for="name">Enter your name:</label>
        <input type="text" id="name" name="name">
        <input type="submit" value="Submit">
    </form>
    
    <?php
    // Handle form data
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
        $name = htmlspecialchars($_POST['name']);
        echo "<p>Hello, $name!</p>";
    }
    ?>
</body>
</html>
