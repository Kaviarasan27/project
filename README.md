# Project Responsive Web Design using Bootstrap
# Date: 20/05/2025
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
    <title>Dribbble Clone</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .navbar-brand {
            font-weight: 700;
            color: #ea4c89 !important;
        }
        
        .hero {
            background-color: #f9f8fd;
            padding: 80px 0;
        }
        
        .card {
            border-radius: 12px;
            overflow: hidden;
            border: none;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .card-img-top {
            height: 200px;
            object-fit: cover;
        }
        
        .btn-primary {
            background-color: #ea4c89;
            border-color: #ea4c89;
        }
        
        .btn-outline-primary {
            color: #ea4c89;
            border-color: #ea4c89;
        }
        
        .btn-outline-primary:hover {
            background-color: #ea4c89;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #d73d7a;
            border-color: #d73d7a;
        }
        
        .category-pill {
            background-color: #f3f3f4;
            padding: 8px 16px;
            border-radius: 20px;
            margin: 5px;
            display: inline-block;
            color: #555;
            font-weight: 500;
            font-size: 14px;
            transition: background-color 0.3s;
        }
        
        .category-pill:hover {
            background-color: #e6e6e8;
            color: #333;
            text-decoration: none;
        }
        
        footer {
            background-color: #333;
            color: #fff;
            padding: 40px 0;
        }
        
        .avatar {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            margin-right: 10px;
        }
        
        .user-info {
            display: flex;
            align-items: center;
            margin-top: 10px;
        }
        
        .search-bar {
            border-radius: 20px;
            background-color: #f3f3f4;
            border: none;
            padding-left: 15px;
        }
        
        .testimonial {
            background-color: #f9f8fd;
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-light bg-white py-3 shadow-sm">
        <div class="container">
            <a class="navbar-brand" href="#"><i class="fab fa-dribbble me-2"></i>dribbble</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#">Inspiration</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Find Work</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Learn Design</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Go Pro</a>
                    </li>
                </ul>
                <form class="d-flex me-3">
                    <input class="form-control search-bar" type="search" placeholder="Search" aria-label="Search">
                </form>
                <button class="btn btn-outline-primary me-2">Log in</button>
                <button class="btn btn-primary">Sign up</button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6 mb-4 mb-lg-0">
                    <h1 class="display-4 fw-bold mb-4">Discover the world's top designers & creatives</h1>
                    <p class="lead mb-4">Dribbble is the leading destination to find & showcase creative work and home to the world's best design professionals.</p>
                    <button class="btn btn-primary btn-lg px-4">Sign up</button>
                </div>
                <div class="col-lg-6">
                    <img src="/static/hero_image.jpg" alt="Hero Image" class="img-fluid rounded-3 shadow">
                </div>
            </div>
        </div>
    </section>

    <!-- Categories Section -->
    <section class="py-5">
        <div class="container">
            <h2 class="text-center mb-4">Browse by category</h2>
            <div class="text-center">
                <a href="#" class="category-pill">Animation</a>
                <a href="#" class="category-pill">Branding</a>
                <a href="#" class="category-pill">Illustration</a>
                <a href="#" class="category-pill">Mobile</a>
                <a href="#" class="category-pill">Print</a>
                <a href="#" class="category-pill">Product Design</a>
                <a href="#" class="category-pill">Typography</a>
                <a href="#" class="category-pill">Web Design</a>
            </div>
        </div>
    </section>

    <!-- Featured Work -->
    <section class="py-5 bg-light">
        <div class="container">
            <div class="d-flex justify-content-between align-items-center mb-4">
                <h2>Popular shots</h2>
                <a href="#" class="text-decoration-none text-dark">View all</a>
            </div>
            <div class="row g-4">
                <!-- Card 1 -->
                <div class="col-md-6 col-lg-4">
                    <div class="card h-100">
                        <img src="/static/mobile_app.webp" class="card-img-top" alt="Design Work">
                        <div class="card-body">
                            <h5 class="card-title">Mobile App Design</h5>
                            <div class="user-info">
                                <img src="/static/mobile_app_person.webp" class="avatar" alt="User">
                                <span>Jane Cooper</span>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Card 2 -->
                <div class="col-md-6 col-lg-4">
                    <div class="card h-100">
                        <img src="/static/brand_id.webp" class="card-img-top" alt="Design Work">
                        <div class="card-body">
                            <h5 class="card-title">Brand Identity</h5>
                            <div class="user-info">
                                <img src="/static/brand_id_person.png" class="avatar" alt="User">
                                <span>Alex Morgan</span>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Card 3 -->
                <div class="col-md-6 col-lg-4">
                    <div class="card h-100">
                        <img src="/static/web_re.webp" class="card-img-top" alt="Design Work">
                        <div class="card-body">
                            <h5 class="card-title">Website Redesign</h5>
                            <div class="user-info">
                                <img src="/static/web_re_person.webp" class="avatar" alt="User">
                                <span>Robert Chen</span>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Card 4 -->
                <div class="col-md-6 col-lg-4">
                    <div class="card h-100">
                        <img src="/static/illustration.webp" class="card-img-top" alt="Design Work">
                        <div class="card-body">
                            <h5 class="card-title">Illustration Set</h5>
                            <div class="user-info">
                                <img src="/static/illustration.jpg" class="avatar" alt="User">
                                <span>Sarah Johnson</span>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Card 5 -->
                <div class="col-md-6 col-lg-4">
                    <div class="card h-100">
                        <img src="/static/logo.webp" class="card-img-top" alt="Design Work">
                        <div class="card-body">
                            <h5 class="card-title">Logo Collection</h5>
                            <div class="user-info">
                                <img src="/static/logo_person.jpg" class="avatar" alt="User">
                                <span>Thomas Wright</span>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Card 6 -->
                <div class="col-md-6 col-lg-4">
                    <div class="card h-100">
                        <img src="/static/ui.webp" class="card-img-top" alt="Design Work">
                        <div class="card-body">
                            <h5 class="card-title">UI Components</h5>
                            <div class="user-info">
                                <img src="/static/ui_person.jpg" class="avatar" alt="User">
                                <span>Maria Garcia</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonial Section -->
    <section class="py-5">
        <div class="container">
            <h2 class="text-center mb-5">Why designers love Dribbble</h2>
            <div class="row">
                <div class="col-md-4 mb-4">
                    <div class="testimonial h-100">
                        <p class="mb-3">"Dribbble has helped me grow as a designer and connect with clients worldwide. It's an essential platform for any creative."</p>
                        <div class="user-info">
                            <img src="/static/ui_last.jpg" class="avatar" alt="User">
                            <div>
                                <strong>Michael Brown</strong>
                                <div class="text-muted">UI Designer</div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 mb-4">
                    <div class="testimonial h-100">
                        <p class="mb-3">"The exposure and feedback I get on Dribbble is invaluable. It's where I showcase my best work and find inspiration."</p>
                        <div class="user-info">
                            <img src="/static/illustrator_last.jpg" class="avatar" alt="User">
                            <div>
                                <strong>Emma Wilson</strong>
                                <div class="text-muted">Illustrator</div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 mb-4">
                    <div class="testimonial h-100">
                        <p class="mb-3">"I landed my dream job through Dribbble. The community here is supportive and the opportunities are endless."</p>
                        <div class="user-info">
                            <img src="/static/product_last.jpg" class="avatar" alt="User">
                            <div>
                                <strong>David Lee</strong>
                                <div class="text-muted">Product Designer</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="py-5 bg-primary text-white text-center">
        <div class="container">
            <h2 class="mb-4">Ready to showcase your work?</h2>
            <p class="lead mb-4">Join the world's leading design community and connect with millions of designers.</p>
            <button class="btn btn-light btn-lg px-4">Get started today</button>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark text-white">
        <div class="container py-5">
            <div class="row">
                <div class="col-lg-4 mb-4 mb-lg-0">
                    <h5 class="mb-3">Dribbble</h5>
                    <p>Dribbble is the world's leading community for creatives to share, grow, and get hired.</p>
                </div>
                <div class="col-md-3 col-lg-2 mb-3 mb-md-0">
                    <h5 class="mb-3">For Designers</h5>
                    <ul class="list-unstyled">
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Go Pro</a></li>
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Explore design work</a></li>
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Design blog</a></li>
                    </ul>
                </div>
                <div class="col-md-3 col-lg-2 mb-3 mb-md-0">
                    <h5 class="mb-3">Hire designers</h5>
                    <ul class="list-unstyled">
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Post a job</a></li>
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Find designers</a></li>
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Brands</a></li>
                    </ul>
                </div>
                <div class="col-md-3 col-lg-2 mb-3 mb-md-0">
                    <h5 class="mb-3">Company</h5>
                    <ul class="list-unstyled">
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">About</a></li>
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Careers</a></li>
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Support</a></li>
                    </ul>
                </div>
                <div class="col-md-3 col-lg-2">
                    <h5 class="mb-3">Directories</h5>
                    <ul class="list-unstyled">
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Design jobs</a></li>
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Designers for hire</a></li>
                        <li class="mb-2"><a href="#" class="text-white text-decoration-none">Tags</a></li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="container border-top border-secondary pt-4">
            <div class="row align-items-center">
                <div class="col-md-6 text-center text-md-start">
                    <p class="mb-md-0">© 2025 A S Siddarth (212224040316). All rights reserved.</p>
                </div>
                <div class="col-md-6">
                    <ul class="list-inline text-center text-md-end mb-0">
                        <li class="list-inline-item me-3">
                            <a href="#" class="text-white"><i class="fab fa-twitter"></i></a>
                        </li>
                        <li class="list-inline-item me-3">
                            <a href="#" class="text-white"><i class="fab fa-facebook-f"></i></a>
                        </li>
                        <li class="list-inline-item me-3">
                            <a href="#" class="text-white"><i class="fab fa-instagram"></i></a>
                        </li>
                        <li class="list-inline-item">
                            <a href="#" class="text-white"><i class="fab fa-pinterest"></i></a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
# OUTPUT:

![alt text](exp10_output1.png)

![alt text](exp10_output2.png)

![alt text](exp10_output3.png)

# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
