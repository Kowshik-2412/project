# Project Responsive Web Design using Bootstrap
# Date: 19-05-2025
# Name: Kowshik P 
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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kowshik's Jersey Shop</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Custom CSS -->
    <style>
        /* Vibrant Hero Section */
        .hero-section {
            background: linear-gradient(135deg, #ff4d4d, #1e90ff);
            padding: 6rem 0;
            color: white;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            position: relative;
            overflow: hidden;
        }
        .hero-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://via.placeholder.com/1200x400?text=Jersey+Shop') center/cover no-repeat;
            opacity: 0.2;
            z-index: 0;
        }
        .hero-content {
            position: relative;
            z-index: 1;
        }

        /* Card Styling */
        .jersey-card {
            transition: transform 0.3s, box-shadow 0.3s;
            border: none;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        .jersey-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.2);
        }
        .card-img-top {
            height: 200px;
            object-fit: cover;
        }
        .price {
            color: #ff4d4d;
            font-weight: bold;
            font-size: 1.2rem;
        }

        /* Navbar Styling */
        .navbar {
            background: linear-gradient(to right, #dc3545, #007bff);
            padding: 0.5rem 0;
        }
        .navbar-brand {
            font-weight: bold;
            color: white !important;
            font-size: 1.5rem;
        }
        .nav-link {
            color: white !important;
            transition: color 0.3s;
        }
        .nav-link:hover {
            color: #ffd700 !important;
        }
        .btn-outline-danger {
            border-color: white;
            color: white;
        }
        .btn-outline-danger:hover {
            background-color: #ffd700;
            color: #dc3545;
            border-color: #ffd700;
        }

        /* Button Styling */
        .btn-danger {
            background: linear-gradient(45deg, #ff4d4d, #ff8c00);
            border: none;
            transition: transform 0.2s;
        }
        .btn-danger:hover {
            transform: scale(1.05);
            background: linear-gradient(45deg, #ff8c00, #ff4d4d);
        }
        .btn-outline-danger {
            transition: background-color 0.3s, color 0.3s;
        }
        .btn-outline-danger:hover {
            background-color: #ffd700;
            color: #dc3545;
        }

        /* Footer Styling */
        footer {
            background: linear-gradient(to right, #212529, #343a40);
            color: white;
        }

        /* Section Background */
        .showcase-section {
            background-color: #f8f9fa;
            padding: 5rem 0;
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <nav class="navbar navbar-expand-lg">
        <div class="container">
            <a class="navbar-brand" href="#">Kowshik's Jersey Shop</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Shop</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Categories</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Contact</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link btn btn-outline-danger ms-2" href="#">Cart</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-section text-center">
        <div class="container hero-content">
            <h1 class="display-4 fw-bold">Score Your Perfect Jersey!</h1>
            <p class="lead">Explore our premium collection of sports jerseys for every fan.</p>
            <a href="#" class="btn btn-danger btn-lg mt-3">Shop Now</a>
        </div>
    </section>

    <!-- Product Showcase Section -->
    <section class="showcase-section">
        <div class="container">
            <h2 class="text-center mb-5 fw-bold" style="color: #dc3545;">Featured Jerseys</h2>
            <div class="row row-cols-1 row-cols-md-3 g-4">
                <!-- Jersey Card 1 -->
                <div class="col">
                    <div class="card jersey-card">
                        <img src="C:\Users\admin\OneDrive\Desktop\10th project\image.png" class="card-img-top" alt="Jersey 1">
                        <div class="card-body">
                            <h5 class="card-title">Team Alpha Jersey</h5>
                            <p class="card-text">High-quality soccer jersey with breathable fabric.</p>
                            <p class="price">$49.99</p>
                            <a href="#" class="btn btn-outline-danger">Add to Cart</a>
                        </div>
                    </div>
                </div>
                <!-- Jersey Card 2 -->
                <div class="col">
                    <div class="card jersey-card">
                        <img src="C:\Users\admin\OneDrive\Desktop\10th project\image copy.png" class="card-img-top" alt="Jersey 2">
                        <div class="card-body">
                            <h5 class="card-title">Basketball Pro Jersey</h5>
                            <p class="card-text">Sleek design for basketball enthusiasts.</p>
                            <p class="price">$59.99</p>
                            <a href="#" class="btn btn-outline-danger">Add to Cart</a>
                        </div>
                    </div>
                </div>
                <!-- Jersey Card 3 -->
                <div class="col">
                    <div class="card jersey-card">
                        <img src="c:\Users\admin\OneDrive\Desktop\10th project\crc jr.jpg" class="card-img-top" alt="Jersey 3">
                        <div class="card-body">
                            <h5 class="card-title">Cricket Classic Jersey</h5>
                            <p class="card-text">Comfortable fit for cricket fans.</p>
                            <p class="price">$44.99</p>
                            <a href="#" class="btn btn-outline-danger">Add to Cart</a>
                        </div>
                    </div>
                </div>
                <!-- IPL Jersey Card -->
                <div class="col">
                    <div class="card jersey-card">
                        <img src="C:\Users\admin\OneDrive\Desktop\10th project\IPL CHN.jpg" class="card-img-top" alt="IPL Jersey">
                        <div class="card-body">
                            <h5 class="card-title">IPL Team Jersey</h5>
                            <p class="card-text">Official IPL jersey for passionate cricket fans.</p>
                            <p class="price">$54.99</p>
                            <a href="#" class="btn btn-outline-danger">Add to Cart</a>
                        </div>
                    </div>
                </div>
                <!-- India Cricket Jersey Card -->
                <div class="col">
                    <div class="card jersey-card">
                        <img src="C:\Users\admin\OneDrive\Desktop\10th project\IND JR.jpg" class="card-img-top" alt="India Cricket Jersey">
                        <div class="card-body">
                            <h5 class="card-title">India Cricket Jersey</h5>
                            <p class="card-text">Official Team India jersey for cricket enthusiasts.</p>
                            <p class="price">$59.99</p>
                            <a href="#" class="btn btn-outline-danger">Add to Cart</a>
                        </div>
                    </div>
                </div>
                <!-- Football Jersey Card -->
                <div class="col">
                    <div class="card jersey-card">
                        <img src="C:\Users\admin\OneDrive\Desktop\10th project\FOOTBALL.jpg" class="card-img-top" alt="Football Jersey">
                        <div class="card-body">
                            <h5 class="card-title">Pro Football Jersey</h5>
                            <p class="card-text">Dynamic football jersey for ultimate performance.</p>
                            <p class="price">$52.99</p>
                            <a href="#" class="btn btn-outline-danger">Add to Cart</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-4 text-center">
        <div class="container">
            <p>© 2025 Kowshik's Jersey Shop. Developed by KOWSHIK P (24900055).</p>
        </div>
    </footer>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>

# OUTPUT:
![image](https://github.com/user-attachments/assets/6900ebcb-ea5d-4e78-9a1a-e49fb19b8c89)
![image](https://github.com/user-attachments/assets/82c72daa-cc8f-413c-bbab-d4029a6bb046)

# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
