# Project Responsive Web Design using Bootstrap
## Date:

## AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.


## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

### Step 5:
Create a HTML file and include the needed Bootstrap components.

### Step 6:
Publish the website in the LocalHost.

## PROGRAM :
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dribbble Clone</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" xintegrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8f8f8;
            color: #333;
        }
        .navbar {
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
        }
        .navbar-brand {
            color: #ea4c89 !important;
        }
        .nav-link {
            color: #555 !important;
            transition: color 0.2s ease;
        }
        .nav-link.active, .nav-link:hover {
            color: #ea4c89 !important;
        }
        .btn-dribbble-primary {
            background-color: #ea4c89;
            border-color: #ea4c89;
            color: white;
            transition: background-color 0.2s ease;
        }
        .btn-dribbble-primary:hover {
            background-color: #d83b77;
            border-color: #d83b77;
            color: white;
        }
        .btn-dribbble-secondary {
            background-color: #f3f3f4;
            border-color: #f3f3f4;
            color: #555;
            transition: background-color 0.2s ease;
        }
        .btn-dribbble-secondary:hover {
            background-color: #e2e2e3;
            border-color: #e2e2e3;
            color: #333;
        }
        .hero-section {
            background-color: #fcfcfc;
            border-bottom: 1px solid #eee;
        }
        .search-bar-hero .form-control {
            border: 1px solid #ddd;
            box-shadow: none;
        }
        .search-bar-hero .input-group-text {
            border: 1px solid #ddd;
            border-right: none;
            color: #888;
        }
        .trending-tags .badge {
            transition: background-color 0.2s ease;
        }
        .trending-tags .badge:hover {
            background-color: #ddd;
            cursor: pointer;
        }
        .design-card {
            border: none;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }
        .design-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.12);
        }
        .design-card img {
            height: 200px;
            object-fit: cover;
        }
        .designer-avatar {
            width: 30px;
            height: 30px;
            object-fit: cover;
        }
        .footer {
            background-color: #fcfcfc;
            border-top: 1px solid #eee;
        }
        .footer ul li a {
            line-height: 2;
            transition: color 0.2s ease;
        }
        .footer ul li a:hover, .footer .social-icons a:hover {
            color: #ea4c89;
        }
        .footer .social-icons a {
            transition: color 0.2s ease;
        }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg navbar-light bg-white sticky-top py-3">
        <div class="container">
            <a class="navbar-brand fw-bold" href="#">Dribbble Clone</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <a class="nav-link active fw-medium" aria-current="page" href="#">Inspiration</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link fw-medium" href="#">Find Work</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link fw-medium" href="#">Learn Design</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link fw-medium" href="#">Go Pro</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link fw-medium" href="#">Hire Designers</a>
                    </li>
                </ul>
                <form class="d-flex me-3">
                    <div class="input-group">
                        <input type="search" class="form-control rounded-pill" placeholder="Search..." aria-label="Search">
                    </div>
                </form>
                <div class="d-flex">
                    <a href="#" class="btn btn-dribbble-secondary rounded-pill me-2">Sign In</a>
                    <a href="#" class="btn btn-dribbble-primary rounded-pill">Sign Up</a>
                </div>
            </div>
        </div>
    </nav>

    <section id="home" class="hero-section py-6 text-center">
        <div class="container">
            <h1 class="display-4 fw-bold mb-4">Discover the world's top designers & creative projects.</h1>
            <p class="lead text-secondary mb-4">Dribbble is the leading destination to find & showcase creative work and home to the world's best design professionals.</p>
            <div class="row justify-content-center mb-4">
                <div class="col-md-8 col-lg-6">
                    <div class="input-group search-bar-hero">
                        <span class="input-group-text rounded-pill ps-4 bg-white border-0 border-end-0"><i class="bi bi-search"></i></span>
                        <input type="text" class="form-control rounded-pill ps-0" placeholder="Search by keyword, tag, or designer..." aria-label="Search">
                    </div>
                </div>
            </div>
            <div class="trending-tags mt-4">
                <strong class="me-2">Trending searches:</strong>
                <span class="badge bg-light text-secondary px-3 py-2 rounded-pill fw-medium m-1">landing page</span>
                <span class="badge bg-light text-secondary px-3 py-2 rounded-pill fw-medium m-1">ui design</span>
                <span class="badge bg-light text-secondary px-3 py-2 rounded-pill fw-medium m-1">branding</span>
                <span class="badge bg-light text-secondary px-3 py-2 rounded-pill fw-medium m-1">illustration</span>
                <span class="badge bg-light text-secondary px-3 py-2 rounded-pill fw-medium m-1">mobile app</span>
                <span class="badge bg-light text-secondary px-3 py-2 rounded-pill fw-medium m-1">web design</span>
            </div>
        </div>
    </section>

    <section id="designs" class="content-section py-5 bg-light">
        <div class="container">
            <div class="text-center mb-5">
                <h2 class="display-5 fw-bold">Explore Inspiring Designs</h2>
                <p class="lead text-muted">A curated collection of the best creative work.</p>
            </div>
            <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 row-cols-lg-4 g-4">
                <div class="col">
                    <div class="card design-card rounded-3 bg-white">
                        <img src="desgn.jpg" class="card-img-top rounded-top-3" alt="Design Shot 1">
                        <div class="card-body p-3">
                            <h5 class="card-title fs-5 fw-semibold mb-2">Minimalist Website UI</h5>
                            <div class="designer-info d-flex align-items-center fs-6 text-secondary">
                                
                                <span>Jane Doe</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card design-card rounded-3 bg-white">
                        <img src="appmockup.png" class="card-img-top rounded-top-3" alt="App Mockup">
                        <div class="card-body p-3">
                            <h5 class="card-title fs-5 fw-semibold mb-2">Mobile App Onboarding</h5>
                            <div class="designer-info d-flex align-items-center fs-6 text-secondary">
                               
                                <span>John Smith</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card design-card rounded-3 bg-white">
                        <img src="branding concept.png" class="card-img-top rounded-top-3" alt="Branding Concept">
                        <div class="card-body p-3">
                            <h5 class="card-title fs-5 fw-semibold mb-2">Brand Identity Design</h5>
                            <div class="designer-info d-flex align-items-center fs-6 text-secondary">
                                
                                <span>Alice Brown</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card design-card rounded-3 bg-white">
                        <img src="aia.jpg" class="card-img-top rounded-top-3" alt="Illustration">
                        <div class="card-body p-3">
                            <h5 class="card-title fs-5 fw-semibold mb-2">Digital Illustration Art</h5>
                            <div class="designer-info d-flex align-items-center fs-6 text-secondary">
                                
                                <span>Bob Johnson</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card design-card rounded-3 bg-white">
                        <img src="analytics.webp" class="card-img-top rounded-top-3" alt="Dashboard UI">
                        <div class="card-body p-3">
                            <h5 class="card-title fs-5 fw-semibold mb-2">Analytics Dashboard UI</h5>
                            <div class="designer-info d-flex align-items-center fs-6 text-secondary">
                                
                                <span>Charlie Davis</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card design-card rounded-3 bg-white">
                        <img src="icon.jpg" class="card-img-top rounded-top-3" alt="Icon Set">
                        <div class="card-body p-3">
                            <h5 class="card-title fs-5 fw-semibold mb-2">Modern Icon Set Design</h5>
                            <div class="designer-info d-flex align-items-center fs-6 text-secondary">
                                
                                <span>Diana Miller</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="footer py-5 text-secondary">
        <div class="container">
            <div class="row">
                <div class="col-lg-3 col-md-6 mb-4 mb-lg-0">
                    <h5 class="mb-3 fw-semibold text-dark">Dribbble Clone</h5>
                    <p>Dribbble is the world's leading community for creatives to share, grow, and get hired.</p>
                    <div class="social-icons">
                        <a href="#" class="me-3 fs-4 text-secondary"><i class="bi bi-dribbble"></i></a>
                        <a href="#" class="me-3 fs-4 text-secondary"><i class="bi bi-twitter"></i></a>
                        <a href="#" class="me-3 fs-4 text-secondary"><i class="bi bi-facebook"></i></a>
                        <a href="#" class="me-3 fs-4 text-secondary"><i class="bi bi-instagram"></i></a>
                        <a href="#" class="fs-4 text-secondary"><i class="bi bi-pinterest"></i></a>
                    </div>
                </div>
                <div class="col-lg-2 col-md-6 mb-4 mb-lg-0">
                    <h5 class="mb-3 fw-semibold text-dark">For designers</h5>
                    <ul class="list-unstyled p-0">
                        <li><a href="#" class="text-secondary text-decoration-none">Go Pro!</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Explore design work</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Design blog</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Overtime podcast</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Playoffs</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Weekly Warm-Up</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Code of conduct</a></li>
                    </ul>
                </div>
                <div class="col-lg-2 col-md-6 mb-4 mb-lg-0">
                    <h5 class="mb-3 fw-semibold text-dark">Hire designers</h5>
                    <ul class="list-unstyled p-0">
                        <li><a href="#" class="text-secondary text-decoration-none">Post a job opening</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Post a freelance project</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Search for designers</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Brands</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Advertise with us</a></li>
                    </ul>
                </div>
                <div class="col-lg-2 col-md-6 mb-4 mb-lg-0">
                    <h5 class="mb-3 fw-semibold text-dark">Company</h5>
                    <ul class="list-unstyled p-0">
                        <li><a href="#" class="text-secondary text-decoration-none">About</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Careers</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Support</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Media kit</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Testimonials</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">API</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Terms of service</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Privacy policy</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Cookie policy</a></li>
                    </ul>
                </div>
                <div class="col-lg-3 col-md-6 mb-4 mb-lg-0">
                    <h5 class="mb-3 fw-semibold text-dark">Directories</h5>
                    <ul class="list-unstyled p-0">
                        <li><a href="#" class="text-secondary text-decoration-none">Design jobs</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Designers for hire</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Freelance designers for hire</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Tags</a></li>
                        <li><a href="#" class="text-secondary text-decoration-none">Places</a></li>
                    </ul>
                </div>
            </div>
            <div class="text-center copyright mt-5 pt-3 border-top border-light">
                <p class="mb-0 fs-6 text-muted">&copy; 2025 Dribbble Clone. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" xintegrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>

## OUTPUT:
![alt text](<../Screenshot 2025-05-25 154412.png>)


## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
