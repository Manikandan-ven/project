# Project Responsive Web Design using Bootstrap
# Date:30.11.2024
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dress Shop</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: 'Pacifico', cursive;
            margin: 0;
            padding: 0;
            background-color: #f9fbe7;
            color: #4e342e;
        }

        .navbar {
            background-color: #6a1b9a;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
        }

        .navbar-brand, .navbar-nav .nav-link {
            color: #ffffff !important;
        }

        .navbar-nav {
            flex-direction: row;
        }

        .navbar-nav .nav-link {
            padding: 0 15px;
        }

        .nav-item .btn-primary {
            background-color: #ff80ab;
            border-color: #ff80ab;
        }

        .nav-item .btn-primary:hover {
            background-color: #d500f9;
            border-color: #d500f9;
        }

        .header-section h3 {
            font-weight: bold;
            color: #6a1b9a;
        }

        .header-section p {
            font-size: 1.2em;
            color: #4e342e;
        }

        .gallery-section {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            padding: 20px;
        }

        .card {
            background-color: #ffffff;
            border: 1px solid #cfd8dc;
            border-radius: 10px;
            box-shadow: 0px 6px 12px rgba(0, 0, 0, 0.08);
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.15);
        }

        .gallery-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 10px 10px 0 0;
        }

        .card-title {
            font-weight: bold;
            font-size: 1.1rem;
            color: #6a1b9a;
            text-align: center;
            margin-top: 15px;
        }

        .card-body {
            padding: 20px;
            text-align: center;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        footer {
            background-color: #6a1b9a;
            color: #ffffff;
            text-align: center;
            padding: 25px;
            font-size: 0.9em;
            margin-top: 40px;
            box-shadow: 0px -2px 5px rgba(0, 0, 0, 0.1);
        }

        @media (max-width: 768px) {
            .navbar-nav {
                flex-direction: column;
                text-align: center;
                padding: 10px 0;
            }

            .gallery-section {
                margin-top: 20px;
            }

            .card-body {
                padding: 10px;
            }
        }

        @media (max-width: 480px) {
            .header-section h3 {
                font-size: 1.5em;
            }

            .header-section p {
                font-size: 1em;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark">
        <a class="navbar-brand" href="#">Dress Shop</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ml-auto">
                <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Collections</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Sales</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
                <li class="nav-item"><a class="btn btn-primary" href="#">Sign Up</a></li>
            </ul>
        </div>
    </nav>

    <div class="container mt-4">
        <div class="text-center mb-4 header-section">
            <h4>Fashion Forward</h4>
            <h3>"Style Redefined, Elegance Redressed!"</h3>
            <p class="lead">"Discover the latest trends and timeless classics in our dress shop"</p>
        </div>

        <div class="gallery-section">
            <div class="card">
                <img src="evening.jpg" class="gallery-img"alt="Evening Dress">
                <div class="card-body">
                    <p class="card-title">EVENING DRESS</p>
                    <small class="text-muted">Versace</small>
                </div>
            </div>
            <div class="card">
                <img src="casual - Copy.jpg" class="gallery-img" alt="Casual Dress">
                <div class="card-body">
                    <p class="card-title">CASUAL DRESS</p>
                    <small class="text-muted">H&M</small>
                </div>
            </div>
            <div class="card">
                <img src="formal.jpg" class="gallery-img" alt="Formal Dress">
                <div class="card-body">
                    <p class="card-title">FORMAL DRESS</p>
                    <small class="text-muted">Zara</small>
                </div>
            </div>
            <div class="card">
                <img src="party wear.jpg" class="gallery-img" alt="Party Wear">
                <div class="card-body">
                    <p class="card-title">PARTY WEAR</p>
                    <small class="text-muted">Gucci</small>
                </div>
            </div>
            <div class="card">
                <img src="trational image.jpg"gallery-img" alt="Traditional Wear">
                <div class="card-body">
                    <p class="card-title">TRADITIONAL WEAR</p>
                    <small class="text-muted">Fabindia</small>
                </div>
            </div>
            <div class="card">
                <img src="summer.jpg" class="gallery-img" alt="Summer Dress">
                <div class="card-body">
                    <p class="card-title">SUMMER DRESS</p>
                    <small class="text-muted">Forever 21</small>
                </div>
            </div>
        </div>
    </div>

    <footer class="bg-dark text-white text-center py-3">
        <p>© Dress Shop. All rights reserved.</p>
        <p>Designed by MANIKANDAN.V</p> 
    </footer>

    <script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.bundle.min.js"></script>
</body>
</html>


```
# OUTPUT:
![Screenshot 2024-12-25 081256](https://github.com/user-attachments/assets/6d1f468c-bb98-4c7e-bd63-518be75dc234)

![Screenshot 2024-12-25 081328](https://github.com/user-attachments/assets/bc7ae072-465b-4a79-98e8-b59c6cef2ead)

# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
