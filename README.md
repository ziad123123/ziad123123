<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Z Phone</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
ق
        header {
            background: #2f4f4f;
            color: white;
            text-align: center;
            padding: 1.5em 0;
            font-family: 'Times New Roman', serif;
        }

        header h1 {
            margin: 0;
            font-size: 3em;
        }

        nav ul {
            list-style: none;
            padding: 0;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-size: 18px;
            cursor: pointer;
            font-family: 'Times New Roman', serif;
        }

        section {
            display: none;
            padding: 2em;
            text-align: center;
        }

        section.active {
            display: block;
        }

        /* Classic style for the homepage */
        #home {
            background-color: #fff8f0;
            padding: 50px 20px;
            font-family: 'Georgia', serif;
            color: #333;
            text-align: center;
        }

        #home h2 {
            font-size: 2.5em;
            margin-bottom: 20px;
        }

        #home p {
            font-size: 1.2em;
            margin-bottom: 30px;
        }

        .shop-now-btn {
            padding: 1em 2em;
            background-color: #2f4f4f;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.2em;
            cursor: pointer;
            text-decoration: none;
            transition: background-color 0.3s ease;
        }

        .shop-now-btn:hover {
            background-color: #006400;
        }

        /* Styling Contact Section */
        #contact {
            background-color: #fff8f0;
            padding: 50px 20px;
            font-family: 'Georgia', serif;
            color: #333;
            text-align: center;
        }

        #contact h2 {
            font-size: 2.5em;
            margin-bottom: 30px;
        }

        .contact-container {
            max-width: 600px;
            margin: 0 auto;
            background-color: white;
            border: 3px solid #2f4f4f;
            border-radius: 10px;
            padding: 20px 30px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }

        form label {
            display: block;
            margin-bottom: 10px;
            font-size: 1.1em;
            font-weight: bold;
            color: #2f4f4f;
        }

        form input, form textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            border: 2px solid #ccc;
            border-radius: 5px;
            font-size: 1em;
            font-family: 'Georgia', serif;
            box-sizing: border-box;
        }

        form input:focus, form textarea:focus {
            border-color: #2f4f4f;
            outline: none;
            box-shadow: 0 0 5px rgba(47, 79, 79, 0.5);
        }

        form textarea {
            height: 150px;
            resize: none;
        }

        form button {
            padding: 10px 20px;
            background-color: #2f4f4f;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.2em;
            cursor: pointer;
            transition: background-color 0.3s ease;
            font-family: 'Georgia', serif;
        }

        form button:hover {
            background-color: #006400;
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <h1>Z Phone</h1>
        <nav>
            <ul>
                <li><a href="#" onclick="showSection('home')">Home</a></li>
                <li><a href="#" onclick="showSection('products')">Products</a></li>
                <li><a href="#" onclick="showSection('about')">About</a></li>
                <li><a href="#" onclick="showSection('contact')">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Home Section -->
    <section id="home" class="active">
        <h2>Welcome to Z Phone</h2>
        <p>Explore our wide range of tech products tailored to meet your needs.</p>
        <a href="#products" class="shop-now-btn" onclick="showSection('products')">Shop Now</a>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Us</h2>
        <div class="contact-container">
            <form>
                <label for="name">Full Name</label>
                <input type="text" id="name" placeholder="Enter your full name" required>

                <label for="email">Email</label>
                <input type="email" id="email" placeholder="Enter your email address" required>

                <label for="message">Your Message</label>
                <textarea id="message" placeholder="Write your message here" required></textarea>

                <button type="submit">Send Message</button>
            </form>
        </div>
    </section>

    <script>
        // Function to show the selected section
        function showSection(sectionId) {
            document.querySelectorAll("section").forEach(section => section.classList.remove("active"));
            document.getElementById(sectionId).classList.add("active");
        }
    </script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
}

header {
    background: #007BFF;
    color: white;
    text-align: center;
    padding: 1em 0;
}

.logo {
    width: 100px;
    margin-top: 10px;
}

section {
    padding: 2em;
    margin: 1em auto;
    max-width: 1200px;
}

.category {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    margin-bottom: 2em;
}

.product {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 1em;
    text-align: center;
    width: 30%;
    margin-bottom: 1em;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.product img {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
}

form {
    max-width: 600px;
    margin: auto;
}

form input, form textarea, form button {
    width: 100%;
    margin-bottom: 1em;
    padding: 0.5em;
    border-radius: 5px;
    border: 1px solid #ddd;
}

document.getElementById('contact-form').addEventListener('submit', function(e) {
    e.preventDefault();
    alert('Thank you for contacting us!');
    this.reset();
});

