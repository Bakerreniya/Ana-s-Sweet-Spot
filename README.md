
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ana's Sweet Spot | Artisan Bakery - Dark</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,500;0,600;1,400&family=Quicksand:wght@300;400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Dark Theme Base Styles */
        :root {
            --dark-bg: #121212;
            --darker-bg: #0a0a0a;
            --card-bg: #1e1e1e;
            --card-border: #333;
            --text-primary: #f5f5f5;
            --text-secondary: #b0b0b0;
            --text-accent: #d4af37;
            --soft-pink: #ff7eb3;
            --dusty-rose: #e8b4bc;
            --deep-rose: #d48a97;
            --cream: #2a2a2a;
            --chocolate: #c19a6b;
            --gold: #d4af37;
            --light-gold: #f4e4b5;
            --accent-dark: #8b5a2b;
            --accent-light: #e8b4bc;
            --shadow-color: rgba(0, 0, 0, 0.5);
            --shadow-light: rgba(0, 0, 0, 0.3);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Quicksand', sans-serif;
            font-weight: 300;
            background-color: var(--dark-bg);
            color: var(--text-primary);
            line-height: 1.7;
            overflow-x: hidden;
        }
        
        h1, h2, h3, .logo {
            font-family: 'Dancing Script', cursive;
            font-weight: 600;
            color: var(--gold);
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Background - Darker Version */
        .page-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(10, 10, 10, 0.85), rgba(10, 10, 10, 0.9)),
                url('https://www.dropbox.com/scl/fi/ofyspzth9gl99x2kk97bh/IMG_7155.jpeg?rlkey=dp20cws62yyci0jpsa65qwx0z&st=pbetxe8a&raw=1');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            z-index: -1;
        }
        
        /* Add overlay to make text more readable */
        .content-overlay {
            position: relative;
            z-index: 1;
        }
        
        /* Make hero section stand out more */
        .hero {
            background-color: rgba(30, 30, 30, 0.85);
            border-radius: 20px;
            margin: 20px;
            padding: 60px 20px;
            box-shadow: 0 10px 30px var(--shadow-color);
            border: 1px solid var(--card-border);
        }
        
        /* Navigation */
        header {
            background-color: rgba(18, 18, 18, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            padding: 15px 0;
            border-bottom: 1px solid var(--card-border);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 2.8rem;
            color: var(--gold);
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .logo span {
            color: var(--deep-rose);
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        
        nav a {
            text-decoration: none;
            color: var(--text-primary);
            font-family: 'Playfair Display', serif;
            font-weight: 500;
            font-size: 1.1rem;
            padding: 8px 15px;
            border-radius: 20px;
            transition: all 0.3s ease;
            position: relative;
        }
        
        nav a:hover {
            color: var(--deep-rose);
            background-color: rgba(212, 138, 151, 0.15);
        }
        
        nav a.active {
            color: var(--deep-rose);
            background-color: rgba(212, 138, 151, 0.2);
        }
        
        nav a.active:after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 50%;
            transform: translateX(-50%);
            width: 5px;
            height: 5px;
            background-color: var(--deep-rose);
            border-radius: 50%;
        }
        
        /* Page Container */
        .page-container {
            min-height: 100vh;
            padding-top: 100px;
            padding-bottom: 60px;
        }
        
        .page {
            display: none;
        }
        
        .page.active {
            display: block;
            animation: fadeIn 0.8s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        /* Hero Section */
        .hero h1 {
            font-size: 4.5rem;
            margin-bottom: 20px;
            color: var(--gold);
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3);
        }
        
        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 40px;
            color: var(--text-secondary);
            font-family: 'Playfair Display', serif;
            font-style: italic;
        }
        
        .cta-button {
            display: inline-block;
            background: linear-gradient(135deg, var(--deep-rose), var(--accent-dark));
            color: white;
            padding: 16px 45px;
            border-radius: 30px;
            text-decoration: none;
            font-size: 1.2rem;
            font-weight: 500;
            box-shadow: 0 6px 20px rgba(212, 138, 151, 0.3);
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-family: 'Quicksand', sans-serif;
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(212, 138, 151, 0.5);
            background: linear-gradient(135deg, var(--dusty-rose), var(--deep-rose));
        }
        
        /* Menu Page */
        .page-title {
            text-align: center;
            font-size: 3.5rem;
            margin-bottom: 50px;
            position: relative;
            padding-bottom: 20px;
        }
        
        .page-title:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--deep-rose), transparent);
        }
        
        .flavors-section {
            margin-bottom: 80px;
        }
        
        .flavors-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .flavor-card {
            background: var(--card-bg);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px var(--shadow-color);
            transition: all 0.4s ease;
            border: 1px solid var(--card-border);
        }
        
        .flavor-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.6);
            border-color: var(--deep-rose);
        }
        
        .flavor-content {
            padding: 25px;
        }
        
        .flavor-content h3 {
            font-size: 1.8rem;
            margin-bottom: 10px;
            color: var(--deep-rose);
        }
        
        .flavor-content p {
            color: var(--text-secondary);
        }
        
        /* Pricing Section */
        .pricing-section {
            margin-bottom: 80px;
        }
        
        .pricing-category {
            margin-bottom: 50px;
        }
        
        .pricing-category h3 {
            font-size: 2.2rem;
            margin-bottom: 30px;
            text-align: center;
            color: var(--chocolate);
        }
        
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
        }
        
        .price-card {
            background: var(--card-bg);
            border-radius: 15px;
            padding: 30px 25px;
            text-align: center;
            box-shadow: 0 8px 25px var(--shadow-color);
            border: 1px solid var(--card-border);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .price-card:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--dusty-rose), var(--gold));
        }
        
        .price-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.6);
            border-color: var(--gold);
        }
        
        .price-card h4 {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: var(--text-primary);
            font-family: 'Playfair Display', serif;
        }
        
        .price {
            font-size: 2.5rem;
            color: var(--deep-rose);
            font-weight: bold;
            margin: 15px 0;
            font-family: 'Playfair Display', serif;
        }
        
        .price-image {
            height: 180px;
            background-size: cover;
            background-position: center;
            border-radius: 10px;
            margin-top: 15px;
            border: 2px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 4px 15px var(--shadow-color);
        }
        
        /* Gallery Section */
        .gallery-section {
            margin: 100px 0;
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }
        
        .gallery-item {
            border-radius: 15px;
            overflow: hidden;
            height: 300px;
            background-size: cover;
            background-position: center;
            box-shadow: 0 8px 25px var(--shadow-color);
            transition: all 0.4s ease;
            position: relative;
            cursor: pointer;
            border: 2px solid rgba(255, 255, 255, 0.05);
        }
        
        .gallery-item:hover {
            transform: scale(1.03);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.7);
            border-color: var(--deep-rose);
        }
        
        /* Policies Section */
        .policies-section {
            margin: 100px 0;
            background-color: var(--card-bg);
            border-radius: 20px;
            padding: 50px;
            box-shadow: 0 10px 30px var(--shadow-color);
            border: 1px solid var(--card-border);
        }
        
        .policy-box {
            background: rgba(40, 40, 40, 0.7);
            border-radius: 15px;
            padding: 30px;
            margin: 30px 0;
            border-left: 5px solid var(--deep-rose);
            box-shadow: 0 5px 20px var(--shadow-light);
        }
        
        .policy-box h3 {
            color: var(--deep-rose);
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        
        .policy-box ul {
            padding-left: 20px;
            margin-bottom: 15px;
        }
        
        .policy-box li {
            margin-bottom: 12px;
            color: var(--text-secondary);
        }
        
        .warning {
            background-color: rgba(255, 193, 7, 0.1);
            border-left: 5px solid #ffc107;
            padding: 20px;
            margin: 20px 0;
            border-radius: 0 10px 10px 0;
            color: #ffd54f;
        }
        
        /* Order Form - Multi Step */
        .order-container {
            max-width: 800px;
            margin: 0 auto;
            background: var(--card-bg);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 40px var(--shadow-color);
            border: 1px solid var(--card-border);
        }
        
        .form-header {
            background: linear-gradient(135deg, var(--accent-dark), var(--deep-rose));
            color: white;
            padding: 25px;
            text-align: center;
        }
        
        .form-header h2 {
            color: white;
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .step-indicator {
            display: flex;
            justify-content: center;
            margin-top: 20px;
            gap: 30px;
        }
        
        .step {
            width: 35px;
            height: 35px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            transition: all 0.3s ease;
            color: white;
        }
        
        .step.active {
            background-color: white;
            color: var(--deep-rose);
            transform: scale(1.1);
        }
        
        .step.completed {
            background-color: var(--light-gold);
            color: var(--darker-bg);
        }
        
        .form-body {
            padding: 40px;
        }
        
        .form-step {
            display: none;
            animation: fadeIn 0.5s ease;
        }
        
        .form-step.active {
            display: block;
        }
        
        .step-title {
            font-size: 2rem;
            margin-bottom: 25px;
            color: var(--gold);
            text-align: center;
            font-family: 'Dancing Script', cursive;
        }
        
        .flavor-options, .size-options {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .option-card {
            border: 2px solid var(--card-border);
            border-radius: 12px;
            padding: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
            background: rgba(40, 40, 40, 0.5);
            color: var(--text-secondary);
        }
        
        .option-card:hover {
            border-color: var(--dusty-rose);
            background-color: rgba(232, 180, 188, 0.1);
            color: var(--text-primary);
        }
        
        .option-card.selected {
            border-color: var(--deep-rose);
            background-color: rgba(232, 180, 188, 0.15);
            box-shadow: 0 5px 15px rgba(212, 138, 151, 0.2);
            color: var(--text-primary);
        }
        
        .option-card h4 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--chocolate);
        }
        
        .upload-area {
            border: 2px dashed var(--dusty-rose);
            border-radius: 15px;
            padding: 40px 20px;
            text-align: center;
            margin: 30px 0;
            cursor: pointer;
            transition: all 0.3s ease;
            background: rgba(40, 40, 40, 0.3);
        }
        
        .upload-area:hover {
            border-color: var(--deep-rose);
            background-color: rgba(232, 180, 188, 0.1);
        }
        
        .upload-icon {
            font-size: 3rem;
            color: var(--dusty-rose);
            margin-bottom: 15px;
        }
        
        .skip-button {
            background: none;
            border: none;
            color: var(--deep-rose);
            text-decoration: underline;
            cursor: pointer;
            font-size: 1rem;
            margin-top: 15px;
            font-family: 'Quicksand', sans-serif;
        }
        
        .terms-box {
            border: 1px solid rgba(232, 180, 188, 0.3);
            border-radius: 12px;
            padding: 25px;
            margin: 30px 0;
            max-height: 300px;
            overflow-y: auto;
            background-color: rgba(30, 30, 30, 0.8);
            color: var(--text-secondary);
        }
        
        .terms-box h4 {
            color: var(--deep-rose);
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .terms-box ul {
            padding-left: 20px;
            margin-bottom: 15px;
        }
        
        .terms-box li {
            margin-bottom: 10px;
        }
        
        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 20px;
            color: var(--text-secondary);
        }
        
        .form-control {
            width: 100%;
            padding: 15px;
            border: 1px solid var(--card-border);
            border-radius: 10px;
            font-size: 1rem;
            font-family: 'Quicksand', sans-serif;
            margin-bottom: 20px;
            transition: all 0.3s ease;
            background-color: rgba(40, 40, 40, 0.7);
            color: var(--text-primary);
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--deep-rose);
            box-shadow: 0 0 0 3px rgba(212, 138, 151, 0.2);
            background-color: rgba(50, 50, 50, 0.7);
        }
        
        .form-navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 40px;
            padding-top: 30px;
            border-top: 1px solid var(--card-border);
        }
        
        .btn {
            padding: 12px 30px;
            border-radius: 25px;
            font-size: 1rem;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s ease;
            font-family: 'Quicksand', sans-serif;
            border: none;
        }
        
        .btn-prev {
            background-color: rgba(40, 40, 40, 0.8);
            color: var(--deep-rose);
            border: 1px solid var(--card-border);
        }
        
        .btn-next, .btn-submit {
            background: linear-gradient(135deg, var(--deep-rose), var(--accent-dark));
            color: white;
        }
        
        .btn-prev:hover {
            background-color: rgba(232, 180, 188, 0.2);
            border-color: var(--dusty-rose);
        }
        
        .btn-next:hover, .btn-submit:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(212, 138, 151, 0.4);
        }
        
        .btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
            transform: none !important;
        }
        
        /* Footer */
        footer {
            background-color: rgba(18, 18, 18, 0.95);
            padding: 40px 0 20px;
            text-align: center;
            border-top: 1px solid var(--card-border);
        }
        
        .footer-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .footer-logo {
            font-size: 2.5rem;
            color: var(--gold);
            margin-bottom: 20px;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 25px 0;
        }
        
        .social-icons a {
            color: var(--text-primary);
            font-size: 1.3rem;
            transition: all 0.3s ease;
        }
        
        .social-icons a:hover {
            color: var(--deep-rose);
            transform: translateY(-3px);
        }
        
        .copyright {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid var(--card-border);
            color: var(--text-secondary);
            font-size: 0.9rem;
        }
        
        /* Theme Toggle Button */
        .theme-toggle {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 50px;
            height: 50px;
            background-color: var(--card-bg);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 4px 15px var(--shadow-color);
            z-index: 1001;
            border: 1px solid var(--card-border);
            transition: all 0.3s ease;
        }
        
        .theme-toggle:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.5);
        }
        
        .theme-toggle i {
            font-size: 1.5rem;
            color: var(--gold);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 15px;
            }
            
            nav ul {
                gap: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 3.2rem;
            }
            
            .page-title {
                font-size: 2.8rem;
            }
            
            .form-body {
                padding: 25px;
            }
            
            .flavor-options, .size-options {
                grid-template-columns: 1fr;
            }
            
            .gallery-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
            
            .policies-section {
                padding: 30px;
            }
            
            .hero {
                margin: 10px;
                padding: 40px 20px;
            }
        }
        
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .logo {
                font-size: 2.2rem;
            }
            
            .page-title {
                font-size: 2.2rem;
            }
            
            .form-navigation {
                flex-direction: column;
                gap: 15px;
            }
            
            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Background - Dark Theme -->
    <div class="page-background"></div>
    
    <!-- Theme Toggle -->
    <div class="theme-toggle" id="themeToggle">
        <i class="fas fa-moon"></i>
    </div>
    
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">Ana's <span>Sweet</span> Spot</div>
            <nav>
                <ul>
                    <li><a href="#" class="nav-link active" data-page="home">Home</a></li>
                    <li><a href="#" class="nav-link" data-page="order">Order</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <!-- Page Container -->
    <div class="page-container content-overlay">
        <!-- Home Page (with Gallery & Policies) -->
        <div id="home" class="page active">
            <div class="hero">
                <div class="container">
                    <h1>Artisan Cakes & Confections</h1>
                    <p>Every cake tells a story, and we're here to help you write yours. Handcrafted with love and the finest ingredients for your special moments.</p>
                    <button class="cta-button start-order">Order Your Custom Cake</button>
                </div>
            </div>
            
            <div class="container">
                <!-- Why Choose Us -->
                <div style="text-align: center; margin-top: 60px;">
                    <h2 style="font-size: 2.8rem; margin-bottom: 30px;">Why Choose Us</h2>
                    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 40px; margin-top: 40px;">
                        <div>
                            <div style="font-size: 3rem; color: var(--deep-rose); margin-bottom: 15px;">🎂</div>
                            <h3 style="font-size: 1.8rem; color: var(--gold);">Custom Designs</h3>
                            <p style="color: var(--text-secondary);">Each cake is uniquely crafted to match your vision and occasion.</p>
                        </div>
                        <div>
                            <div style="font-size: 3rem; color: var(--deep-rose); margin-bottom: 15px;">👩‍🍳</div>
                            <h3 style="font-size: 1.8rem; color: var(--gold);">Artisan Quality</h3>
                            <p style="color: var(--text-secondary);">Made from scratch with premium ingredients and attention to detail.</p>
                        </div>
                        <div>
                            <div style="font-size: 3rem; color: var(--deep-rose); margin-bottom: 15px;">💝</div>
                            <h3 style="font-size: 1.8rem; color: var(--gold);">Made with Love</h3>
                            <p style="color: var(--text-secondary);">Every creation is infused with care and passion for the craft.</p>
                        </div>
                    </div>
                </div>
                
                <!-- Menu Section -->
                <div class="flavors-section">
                    <h2 class="page-title">Our Flavors</h2>
                    <div class="flavors-grid" id="flavorsGrid">
                        <!-- Flavors populated by JS -->
                    </div>
                </div>
                
                <!-- Pricing Section -->
                <div class="pricing-section">
                    <h2 class="page-title">Our Pricing</h2>
                    
                    <div class="pricing-category">
                        <h3>Custom Cakes</h3>
                        <div class="pricing-grid" id="cakePricingGrid">
                            <!-- Cake prices populated by JS -->
                        </div>
                    </div>
                    
                    <div class="pricing-category">
                        <h3>Cupcakes</h3>
                        <div class="pricing-grid" id="cupcakePricingGrid">
                            <!-- Cupcake prices populated by JS -->
                        </div>
                    </div>
                </div>
                
                <!-- Gallery Section -->
                <div class="gallery-section">
                    <h2 class="page-title">Our Gallery</h2>
                    <p style="text-align: center; font-size: 1.2rem; max-width: 800px; margin: 0 auto 50px; color: var(--text-secondary); font-family: 'Playfair Display', serif;">
                        A visual journey through our most cherished creations. Each cake is a masterpiece crafted for special moments.
                    </p>
                    <div class="gallery-grid" id="galleryGrid">
                        <!-- Gallery items populated by JS -->
                    </div>
                </div>
                
                <!-- Policies Section -->
                <div class="policies-section">
                    <h2 class="page-title">Policies & Information</h2>
                    
                    <div class="policy-box">
                        <h3>Booking & Payment</h3>
                        <ul>
                            <li>50% NON-REFUNDABLE DEPOSIT IS REQUIRED AT TIME OF BOOKING!</li>
                            <li>REMAINING BALANCE IS TO BE PAID PRIOR TO PICKUP OR CASH ONLY AT PICKUP!</li>
                            <li>NO CHANGES CAN BE MADE TO YOUR ORDER WITHIN 72 HOURS OF PICKUP!</li>
                        </ul>
                    </div>
                    
                    <div class="policy-box">
                        <h3>Pickup & Care Instructions</h3>
                        <div class="warning">
                            <p><strong>⚠️ Important:</strong> Please arrive at the scheduled pickup time. Late pickup will result in a $20 non-negotiable inconvenience fee.</p>
                        </div>
                        <ul>
                            <li>Ana's Sweet Spot will not be responsible for any damage during transportation or setup after you have picked your order up</li>
                            <li>All cakes are made with buttercream, please keep it out of hot environments to avoid the buttercream melting</li>
                            <li>Cakes/Cupcakes stored in the refrigerator in the box will be good up to 5 days</li>
                            <li>4-6 months in the freezer</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Order Page -->
        <div id="order" class="page">
            <div class="container">
                <h2 class="page-title">Order Your Cake</h2>
                
                <div class="order-container">
                    <!-- FORM WITH GETFORM.IO ENDPOINT -->
                    <form action="https://getform.io/f/azyqlnvb" method="POST" enctype="multipart/form-data" id="cakeOrderForm">
                        <!-- Getform.io hidden fields for better organization -->
                        <input type="hidden" name="_subject" value="🎂 New Cake Order - Ana's Sweet Spot">
                        <input type="hidden" name="_template" value="table">
                        
                        <!-- Hidden fields to store selections -->
                        <input type="hidden" name="Flavor" id="selectedFlavor">
                        <input type="hidden" name="Size" id="selectedSize">
                        <input type="hidden" name="Source" value="Website Order Form">
                        
                        <div class="form-header">
                            <h2>Custom Cake Order</h2>
                            <p>Build your dream cake in 5 simple steps</p>
                            <div class="step-indicator">
                                <div class="step active" data-step="1">1</div>
                                <div class="step" data-step="2">2</div>
                                <div class="step" data-step="3">3</div>
                                <div class="step" data-step="4">4</div>
                                <div class="step" data-step="5">5</div>
                            </div>
                        </div>
                        
                        <div class="form-body">
                            <!-- Step 1: Flavor -->
                            <div class="form-step active" data-step="1">
                                <h3 class="step-title">Choose Your Flavor</h3>
                                <p style="text-align: center; margin-bottom: 30px; color: var(--text-secondary);">Select your favorite cake flavor from our artisan collection</p>
                                <div class="flavor-options" id="orderFlavors">
                                    <!-- Flavors populated by JS -->
                                </div>
                                <div class="form-navigation">
                                    <div></div>
                                    <button type="button" class="btn btn-next" data-next="2">Next →</button>
                                </div>
                            </div>
                            
                            <!-- Step 2: Size -->
                            <div class="form-step" data-step="2">
                                <h3 class="step-title">Select Size & Style</h3>
                                <p style="text-align: center; margin-bottom: 30px; color: var(--text-secondary);">Choose the perfect size and shape for your occasion</p>
                                <div class="size-options" id="orderSizes">
                                    <!-- Size options populated by JS -->
                                </div>
                                <div class="form-navigation">
                                    <button type="button" class="btn btn-prev" data-prev="1">← Back</button>
                                    <button type="button" class="btn btn-next" data-next="3">Next →</button>
                                </div>
                            </div>
                            
                            <!-- Step 3: Inspiration -->
                            <div class="form-step" data-step="3">
                                <h3 class="step-title">Inspiration Photos</h3>
                                <p style="text-align: center; margin-bottom: 30px; color: var(--text-secondary);">Help us visualize your dream cake (optional)</p>
                                
                                <div class="upload-area" id="uploadArea">
                                    <div class="upload-icon">
                                        <i class="fas fa-cloud-upload-alt"></i>
                                    </div>
                                    <h4>Upload Inspiration Photos</h4>
                                    <p>Click to browse photos from your device</p>
                                    <p style="font-size: 0.9rem; color: var(--text-secondary); margin-top: 10px;">Max 5 images, 5MB each</p>
                                    <input type="file" id="fileInput" name="Inspiration Photos" accept="image/*" multiple style="display: none;">
                                </div>
                                
                                <div id="previewArea" style="display: none;">
                                    <div style="display: flex; gap: 15px; flex-wrap: wrap; margin: 20px 0;" id="imagePreviews"></div>
                                </div>
                                
                                <div style="text-align: center;">
                                    <button type="button" class="skip-button" id="skipUpload">Skip this step →</button>
                                </div>
                                
                                <div class="form-navigation">
                                    <button type="button" class="btn btn-prev" data-prev="2">← Back</button>
                                    <button type="button" class="btn btn-next" data-next="4">Next →</button>
                                </div>
                            </div>
                            
                            <!-- Step 4: Terms -->
                            <div class="form-step" data-step="4">
                                <h3 class="step-title">Terms & Conditions</h3>
                                <p style="text-align: center; margin-bottom: 30px; color: var(--text-secondary);">Please review our policies before proceeding</p>
                                
                                <div class="terms-box">
                                    <h4>Ordering Policies</h4>
                                    <ul>
                                        <li>A 50% non-refundable deposit is required at time of booking</li>
                                        <li>Remaining balance must be paid prior to pickup or cash only at pickup</li>
                                        <li>No changes can be made to your order within 72 hours of pickup</li>
                                        <li>Please arrive at your scheduled pickup time to avoid a $20 inconvenience fee</li>
                                        <li>We are not responsible for damage during transportation after pickup</li>
                                        <li>All cakes are made with buttercream - keep out of hot environments</li>
                                        <li>Storage: Refrigerator - up to 5 days, Freezer - 4-6 months</li>
                                    </ul>
                                    <p><strong>By proceeding, you agree to these terms and conditions.</strong></p>
                                </div>
                                
                                <div class="checkbox-group">
                                    <input type="checkbox" id="agreeTerms" name="Agreed to Terms" value="Yes" required>
                                    <label for="agreeTerms">I have read and agree to the terms & conditions</label>
                                </div>
                                
                                <div class="form-navigation">
                                    <button type="button" class="btn btn-prev" data-prev="3">← Back</button>
                                    <button type="button" class="btn btn-next" id="toContactStep" data-next="5" disabled>Next →</button>
                                </div>
                            </div>
                            
                            <!-- Step 5: Contact -->
                            <div class="form-step" data-step="5">
                                <h3 class="step-title">Contact Information</h3>
                                <p style="text-align: center; margin-bottom: 30px; color: var(--text-secondary);">We'll contact you to confirm details and request deposit</p>
                                
                                <div class="form-group">
                                    <input type="text" class="form-control" id="customerName" name="Full Name" placeholder="Full Name *" required>
                                </div>
                                
                                <div class="form-group">
                                    <input type="tel" class="form-control" id="customerPhone" name="Phone Number" placeholder="Phone Number *" required>
                                </div>
                                
                                <div class="form-group">
                                    <input type="email" class="form-control" id="customerEmail" name="Email" placeholder="Email Address *" required>
                                </div>
                                
                                <div class="form-group">
                                    <input type="date" class="form-control" id="pickupDate" name="Pickup Date" required>
                                    <small style="display: block; margin-top: 5px; color: var(--text-secondary);">Please allow 3-5 days for custom orders</small>
                                </div>
                                
                                <div class="form-group">
                                    <textarea class="form-control" id="specialInstructions" name="Special Instructions" rows="4" placeholder="Any special instructions, design details, or notes..."></textarea>
                                </div>
                                
                                <div class="form-navigation">
                                    <button type="button" class="btn btn-prev" data-prev="4">← Back</button>
                                    <button type="submit" class="btn btn-submit">Submit Order</button>
                                </div>
                            </div>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">Ana's Sweet Spot</div>
                <p style="max-width: 600px; margin: 0 auto 20px; color: var(--text-secondary);">Creating beautiful, delicious custom cakes for all your special occasions.</p>
                
                <div class="social-icons">
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-facebook"></i></a>
                    <a href="#"><i class="fab fa-tiktok"></i></a>
                    <a href="#"><i class="fas fa-envelope"></i></a>
                </div>
                
                <div style="color: var(--text-secondary); margin-top: 20px;">
                    <p><i class="fas fa-phone" style="margin-right: 8px;"></i> (770) 765-5783</p>
                    <p><i class="fas fa-clock" style="margin-right: 8px;"></i> Custom orders require 3-5 days notice</p>
                </div>
                
                <div class="copyright">
                    &copy; 2024 Ana's Sweet Spot Bakery. All rights reserved.
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Data from your images
        const flavors = [
            { name: "Classic Vanilla", description: "Vanilla Cake with Vanilla Buttercream" },
            { name: "Classic Strawberry", description: "Strawberry Cake with Vanilla Buttercream" },
            { name: "Strawberry Shortcake", description: "Vanilla Batter with Freshly Diced Strawberries, Strawberry Filling & Vanilla Buttercream" },
            { name: "Red Velvet", description: "Red Velvet Cake with Cream Cheese Filling & Vanilla Buttercream" },
            { name: "Cookies & Creme", description: "Cookies & Creme Cake with Cookies & Creme Filling & Vanilla Buttercream" },
            { name: "Banana Pudding", description: "Banana Pudding Cake with Freshly Sliced Bananas & Vanilla Buttercream" },
            { name: "Birthday Cake", description: "Vanilla Batter with Sprinkles & Vanilla Buttercream" },
            { name: "Chocolate Fudge", description: "Chocolate Cake with Milk Chocolate Buttercream" }
        ];

        const cakePrices = [
            { 
                name: "6\" Round Cake", 
                price: "$150", 
                image: "https://www.dropbox.com/scl/fi/5ymae9cap6qri4ap6kaof/IMG_7172.jpeg?rlkey=awuxg4eb8lfau6fgjqtf5yi5r&st=pznneqwd&raw=1",
                category: "round"
            },
            { 
                name: "8\" Round Cake", 
                price: "$200", 
                image: "https://www.dropbox.com/scl/fi/g0cahv6jz4wb5fno75j42/IMG_7171.jpeg?rlkey=yuhz47vydyleyn11p80cvaqxb&st=i533129f&raw=1",
                category: "round"
            },
            { 
                name: "10\" Round Cake", 
                price: "$260", 
                image: "https://www.dropbox.com/scl/fi/ck7d59wc1q40ji3vpjutr/IMG_7174.jpeg?rlkey=f7iv7hfqa0vyoxegl61pwlzx4&st=r7kbxaih&raw=1",
                category: "round"
            },
            { 
                name: "6\" Heart Cake", 
                price: "$175", 
                image: "https://www.dropbox.com/scl/fi/gxecutfdayy40ih17m1vh/IMG_7173.jpeg?rlkey=pt6y70i0t1a6jgxmp181smwxh&st=sti0kju9&raw=1",
                category: "special"
            },
            { 
                name: "8\" Heart Cake", 
                price: "$225", 
                image: "https://www.dropbox.com/scl/fi/gxecutfdayy40ih17m1vh/IMG_7173.jpeg?rlkey=pt6y70i0t1a6jgxmp181smwxh&st=sti0kju9&raw=1",
                category: "special"
            },
            { 
                name: "10\" Star Cake", 
                price: "$250", 
                image: "https://www.dropbox.com/scl/fi/1eitnm7mtups3x3ddxv0c/IMG_7147.jpeg?rlkey=9v054qiyx3ptanjsfn8y859gz&st=uzmk2daw&raw=1",
                category: "special"
            },
            { 
                name: "8\"+6\" Two Tier Cake", 
                price: "$325", 
                image: "https://www.dropbox.com/scl/fi/3sq07g2l4jwgfpxcah94r/IMG_7170.jpeg?rlkey=c73z1d752tkz9rpepj0oyyawh&st=ew4kw5nx&raw=1",
                category: "tiered"
            },
            { 
                name: "10\"+6\" Two Tier Cake", 
                price: "$385", 
                image: "https://www.dropbox.com/scl/fi/kitx40sr54wf6yx2pujgg/IMG_7166.jpeg?rlkey=pfu59jjf74zcroo0erhjn8rld&st=zc0p4u9g&raw=1",
                category: "tiered"
            }
        ];

        const cupcakePrices = [
            { 
                name: "Assorted Cupcakes", 
                price: "$40", 
                image: "https://www.dropbox.com/scl/fi/z0ehvmntvomjmrt6tzk45/IMG_7168.jpeg?rlkey=m3ilx66qy11o0fak8iwv779fq&st=m3x0kzkv&raw=1",
                description: "Dozen"
            },
            { 
                name: "Customized Cupcakes", 
                price: "$60", 
                image: "https://www.dropbox.com/scl/fi/5qak7f684v844ypopql05/IMG_7167.jpeg?rlkey=q6zf23dadruo20dp8o5roi62p&st=a0s3pq9z&raw=1",
                description: "Dozen"
            },
            { 
                name: "Drunken Infused Cupcakes", 
                price: "$75", 
                image: "https://www.dropbox.com/scl/fi/2d76i4li52vaux038ejtd/IMG_7150.jpeg?rlkey=hr0674y0rdfr1b5xvamxldlym&st=xy90lae3&raw=1",
                description: "Dozen"
            }
        ];

        const galleryImages = [
            "https://www.dropbox.com/scl/fi/8pbg2hcllmw6m9u2g0od6/IMG_7178.jpeg?rlkey=wu9il6yarwiq76351g50z6i16&st=e0dua1gd&raw=1",
            "https://www.dropbox.com/scl/fi/4bfq6qc7q10skrdy6zr61/IMG_7179.jpeg?rlkey=m53t1x17aac3ob5r5ydbj7qzl&st=8gkf17yc&raw=1",
            "https://www.dropbox.com/scl/fi/b847u7iurb967ncldbmi1/IMG_7180.jpeg?rlkey=u9apsni5xhux06yt0arfss8rm&st=30x4xiyu&raw=1",
            "https://www.dropbox.com/scl/fi/n3kmu80n1uanftiwmlk8d/IMG_7181.jpeg?rlkey=iaghzr03p9qlthaep4w4nrzkf&st=dm0di0bx&raw=1",
            "https://www.dropbox.com/scl/fi/857xaym8azjg9b5gf02cz/IMG_7182.jpeg?rlkey=8icpnoc86qtrci5pm30aokz5i&st=r0ozg5sk&raw=1",
            "https://www.dropbox.com/scl/fi/iisjio3qr319tah5kigz7/IMG_7183.jpeg?rlkey=4ef7i03xai6vf9pm9345e6i25&st=3jo5fjjk&raw=1",
            "https://www.dropbox.com/scl/fi/ykwpmmz5aga9euzolkiml/IMG_7185.jpeg?rlkey=vemti024m84nfhpjfdj1e5voo&st=hj2j2q64&raw=1",
            "https://www.dropbox.com/scl/fi/vvtx88lijz7wlrtdft1g0/IMG_7186.jpeg?rlkey=5v8ocsm4yxf1q4cowqpqabo3e&st=u2dk0jlu&raw=1"
        ];

        // Order form data
        let orderData = {
            flavor: null,
            size: null,
            inspirationPhotos: [],
            agreedToTerms: false
        };

        // DOM Content Loaded
        document.addEventListener('DOMContentLoaded', function() {
            // Initialize the website
            populateHomePage();
            initOrderForm();
            setupNavigation();
            setupEventListeners();
            
            // Set minimum date for pickup (tomorrow)
            const today = new Date();
            const tomorrow = new Date(today);
            tomorrow.setDate(tomorrow.getDate() + 1);
            const minDate = tomorrow.toISOString().split('T')[0];
            document.getElementById('pickupDate').min = minDate;
            document.getElementById('pickupDate').value = minDate;
            
            // Setup form validation
            setupFormValidation();
            
            // Setup theme toggle
            setupThemeToggle();
        });

        // Populate Home Page
        function populateHomePage() {
            // Populate flavors
            const flavorsGrid = document.getElementById('flavorsGrid');
            flavors.forEach(flavor => {
                const flavorCard = document.createElement('div');
                flavorCard.className = 'flavor-card';
                flavorCard.innerHTML = `
                    <div class="flavor-content">
                        <h3>${flavor.name}</h3>
                        <p>${flavor.description}</p>
                    </div>
                `;
                flavorsGrid.appendChild(flavorCard);
            });

            // Populate cake prices
            const cakePricingGrid = document.getElementById('cakePricingGrid');
            cakePrices.forEach(cake => {
                const priceCard = document.createElement('div');
                priceCard.className = 'price-card';
                priceCard.innerHTML = `
                    <h4>${cake.name}</h4>
                    <div class="price">${cake.price}</div>
                    ${cake.image ? `<div class="price-image" style="background-image: url('${cake.image}')"></div>` : ''}
                `;
                cakePricingGrid.appendChild(priceCard);
            });

            // Populate cupcake prices
            const cupcakePricingGrid = document.getElementById('cupcakePricingGrid');
            cupcakePrices.forEach(cupcake => {
                const priceCard = document.createElement('div');
                priceCard.className = 'price-card';
                priceCard.innerHTML = `
                    <h4>${cupcake.name}</h4>
                    <div class="price">${cupcake.price}</div>
                    <p style="color: var(--text-secondary); margin-bottom: 10px;">${cupcake.description}</p>
                    ${cupcake.image ? `<div class="price-image" style="background-image: url('${cupcake.image}')"></div>` : ''}
                `;
                cupcakePricingGrid.appendChild(priceCard);
            });

            // Populate gallery
            const galleryGrid = document.getElementById('galleryGrid');
            galleryImages.forEach(image => {
                const galleryItem = document.createElement('div');
                galleryItem.className = 'gallery-item';
                galleryItem.style.backgroundImage = `url('${image}')`;
                galleryGrid.appendChild(galleryItem);
            });
        }

        // Initialize Order Form
        function initOrderForm() {
            // Populate flavor options
            const flavorOptions = document.getElementById('orderFlavors');
            flavors.forEach(flavor => {
                const option = document.createElement('div');
                option.className = 'option-card';
                option.dataset.value = flavor.name;
                option.innerHTML = `
                    <h4>${flavor.name}</h4>
                    <p style="font-size: 0.9rem; color: var(--text-secondary);">${flavor.description}</p>
                `;
                option.addEventListener('click', () => selectOption(option, 'flavor'));
                flavorOptions.appendChild(option);
            });

            // Populate size options
            const sizeOptions = document.getElementById('orderSizes');
            cakePrices.forEach(cake => {
                const option = document.createElement('div');
                option.className = 'option-card';
                option.dataset.value = cake.name;
                option.dataset.price = cake.price;
                option.innerHTML = `
                    <h4>${cake.name}</h4>
                    <div style="color: var(--deep-rose); font-weight: bold; margin: 10px 0;">${cake.price}</div>
                `;
                option.addEventListener('click', () => selectOption(option, 'size'));
                sizeOptions.appendChild(option);
            });

            // Add cupcake options
            cupcakePrices.forEach(cupcake => {
                const option = document.createElement('div');
                option.className = 'option-card';
                option.dataset.value = cupcake.name;
                option.dataset.price = cupcake.price;
                option.innerHTML = `
                    <h4>${cupcake.name}</h4>
                    <div style="color: var(--deep-rose); font-weight: bold; margin: 10px 0;">${cupcake.price}</div>
                    <p style="font-size: 0.9rem; color: var(--text-secondary);">${cupcake.description}</p>
                `;
                option.addEventListener('click', () => selectOption(option, 'size'));
                sizeOptions.appendChild(option);
            });
        }

        // Setup Navigation
        function setupNavigation() {
            // Page navigation
            const navLinks = document.querySelectorAll('.nav-link');
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const pageId = this.dataset.page;
                    
                    // Update active nav link
                    navLinks.forEach(l => l.classList.remove('active'));
                    this.classList.add('active');
                    
                    // Show selected page
                    const pages = document.querySelectorAll('.page');
                    pages.forEach(page => page.classList.remove('active'));
                    document.getElementById(pageId).classList.add('active');
                    
                    // Scroll to top
                    window.scrollTo({ top: 0, behavior: 'smooth' });
                });
            });

            // Order button on home page
            document.querySelector('.start-order').addEventListener('click', function() {
                navLinks.forEach(l => l.classList.remove('active'));
                document.querySelector('.nav-link[data-page="order"]').classList.add('active');
                
                const pages = document.querySelectorAll('.page');
                pages.forEach(page => page.classList.remove('active'));
                document.getElementById('order').classList.add('active');
                
                window.scrollTo({ top: 0, behavior: 'smooth' });
            });
        }

        // Setup Event Listeners
        function setupEventListeners() {
            // File upload
            const uploadArea = document.getElementById('uploadArea');
            const fileInput = document.getElementById('fileInput');
            const skipButton = document.getElementById('skipUpload');
            const previewArea = document.getElementById('previewArea');
            const imagePreviews = document.getElementById('imagePreviews');

            uploadArea.addEventListener('click', () => fileInput.click());
            
            fileInput.addEventListener('change', function() {
                const files = Array.from(this.files).slice(0, 5);
                orderData.inspirationPhotos = files;
                
                // Show previews
                imagePreviews.innerHTML = '';
                files.forEach(file => {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        const img = document.createElement('div');
                        img.style.width = '100px';
                        img.style.height = '100px';
                        img.style.backgroundImage = `url(${e.target.result})`;
                        img.style.backgroundSize = 'cover';
                        img.style.backgroundPosition = 'center';
                        img.style.borderRadius = '8px';
                        img.style.border = '2px solid var(--dusty-rose)';
                        imagePreviews.appendChild(img);
                    };
                    reader.readAsDataURL(file);
                });
                
                previewArea.style.display = 'block';
            });

            skipButton.addEventListener('click', function() {
                orderData.inspirationPhotos = [];
                previewArea.style.display = 'none';
                // Move to next step
                navigateToStep(4);
            });

            // Terms checkbox
            document.getElementById('agreeTerms').addEventListener('change', function() {
                orderData.agreedToTerms = this.checked;
                document.getElementById('toContactStep').disabled = !this.checked;
            });

            // Form navigation
            document.querySelectorAll('.btn-next').forEach(btn => {
                btn.addEventListener('click', function() {
                    const nextStep = this.dataset.next;
                    navigateToStep(nextStep);
                });
            });

            document.querySelectorAll('.btn-prev').forEach(btn => {
                btn.addEventListener('click', function() {
                    const prevStep = this.dataset.prev;
                    navigateToStep(prevStep);
                });
            });
        }

        // Setup Form Validation
        function setupFormValidation() {
            const form = document.getElementById('cakeOrderForm');
            
            form.addEventListener('submit', function(e) {
                // Get current step
                const currentStep = document.querySelector('.form-step.active').dataset.step;
                
                // If not on step 5, prevent submission
                if (currentStep !== '5') {
                    e.preventDefault();
                    alert('Please complete all steps before submitting.');
                    return;
                }
                
                // Validate required fields
                const name = document.getElementById('customerName').value;
                const phone = document.getElementById('customerPhone').value;
                const email = document.getElementById('customerEmail').value;
                const pickupDate = document.getElementById('pickupDate').value;
                const agreed = document.getElementById('agreeTerms').checked;
                
                if (!name || !phone || !email || !pickupDate || !agreed) {
                    e.preventDefault();
                    alert('Please fill in all required fields and agree to the terms.');
                    return;
                }
                
                // Set hidden fields with selected values
                document.getElementById('selectedFlavor').value = orderData.flavor || 'Not selected';
                document.getElementById('selectedSize').value = orderData.size ? orderData.size.name + ' - ' + orderData.size.price : 'Not selected';
                
                // Show success message
                alert('Thank you! Your order has been submitted. We will contact you within 24 hours.');
                
                // Reset form after submission
                setTimeout(() => {
                    resetOrderForm();
                    document.querySelector('.nav-link[data-page="home"]').click();
                }, 1000);
            });
        }

        // Setup Theme Toggle
        function setupThemeToggle() {
            const themeToggle = document.getElementById('themeToggle');
            const themeIcon = themeToggle.querySelector('i');
            
            themeToggle.addEventListener('click', function() {
                // Toggle between dark and light theme
                if (document.body.classList.contains('light-theme')) {
                    // Switch to dark theme
                    document.body.classList.remove('light-theme');
                    themeIcon.className = 'fas fa-moon';
                    document.title = "Ana's Sweet Spot | Artisan Bakery - Dark";
                } else {
                    // Switch to light theme
                    document.body.classList.add('light-theme');
                    themeIcon.className = 'fas fa-sun';
                    document.title = "Ana's Sweet Spot | Artisan Bakery - Light";
                }
            });
        }

        // Helper Functions
        function selectOption(element, type) {
            // Remove selected class from all options of this type
            const allOptions = element.parentElement.querySelectorAll('.option-card');
            allOptions.forEach(opt => opt.classList.remove('selected'));
            
            // Add selected class to clicked option
            element.classList.add('selected');
            
            // Store selection
            if (type === 'flavor') {
                orderData.flavor = element.dataset.value;
            } else if (type === 'size') {
                orderData.size = {
                    name: element.dataset.value,
                    price: element.dataset.price
                };
            }
        }

        function navigateToStep(stepNumber) {
            // Update step indicator
            document.querySelectorAll('.step').forEach(step => {
                step.classList.remove('active');
                if (parseInt(step.dataset.step) < stepNumber) {
                    step.classList.add('completed');
                } else {
                    step.classList.remove('completed');
                }
            });
            document.querySelector(`.step[data-step="${stepNumber}"]`).classList.add('active');
            
            // Show the corresponding form step
            document.querySelectorAll('.form-step').forEach(step => {
                step.classList.remove('active');
            });
            document.querySelector(`.form-step[data-step="${stepNumber}"]`).classList.add('active');
            
            // Scroll to top of form
            document.querySelector('.form-body').scrollTop = 0;
        }

        function resetOrderForm() {
            // Reset order data
            orderData = {
                flavor: null,
                size: null,
                inspirationPhotos: [],
                agreedToTerms: false
            };
            
            // Reset UI
            document.querySelectorAll('.option-card').forEach(card => {
                card.classList.remove('selected');
            });
            
            document.getElementById('agreeTerms').checked = false;
            document.getElementById('toContactStep').disabled = true;
            
            document.getElementById('customerName').value = '';
            document.getElementById('customerPhone').value = '';
            document.getElementById('customerEmail').value = '';
            document.getElementById('specialInstructions').value = '';
            
            // Set pickup date to tomorrow
            const today = new Date();
            const tomorrow = new Date(today);
            tomorrow.setDate(tomorrow.getDate() + 1);
            const minDate = tomorrow.toISOString().split('T')[0];
            document.getElementById('pickupDate').value = minDate;
            
            // Reset file upload
            document.getElementById('fileInput').value = '';
            document.getElementById('previewArea').style.display = 'none';
            document.getElementById('imagePreviews').innerHTML = '';
            
            // Go back to step 1
            navigateToStep(1);
        }
    </script>

    <style>
        /* Light Theme Styles (Toggle) */
        body.light-theme {
            background-color: #fffaf3;
            color: #555;
        }
        
        body.light-theme .page-background {
            background-image: 
                linear-gradient(rgba(255, 255, 255, 0.85), rgba(255, 255, 255, 0.9)),
                url('https://www.dropbox.com/scl/fi/ofyspzth9gl99x2kk97bh/IMG_7155.jpeg?rlkey=dp20cws62yyci0jpsa65qwx0z&st=pbetxe8a&raw=1');
        }
        
        body.light-theme h1,
        body.light-theme h2,
        body.light-theme h3,
        body.light-theme .logo {
            color: #6d4c41;
        }
        
        body.light-theme .hero {
            background-color: rgba(255, 255, 255, 0.85);
            border: 1px solid rgba(232, 180, 188, 0.3);
        }
        
        body.light-theme header {
            background-color: rgba(255, 255, 255, 0.95);
            border-bottom: 1px solid rgba(232, 180, 188, 0.3);
        }
        
        body.light-theme nav a {
            color: #6d4c41;
        }
        
        body.light-theme .flavor-card,
        body.light-theme .price-card,
        body.light-theme .order-container,
        body.light-theme .policy-box,
        body.light-theme .terms-box {
            background: white;
            border-color: rgba(232, 180, 188, 0.3);
        }
        
        body.light-theme .form-control {
            background-color: white;
            color: #555;
            border-color: rgba(232, 180, 188, 0.5);
        }
        
        body.light-theme footer {
            background-color: rgba(255, 255, 255, 0.95);
            border-top: 1px solid rgba(232, 180, 188, 0.3);
        }
        
        body.light-theme .copyright {
            color: #888;
        }
        
        body.light-theme .theme-toggle {
            background-color: white;
            border-color: rgba(232, 180, 188, 0.3);
        }
        
        body.light-theme .theme-toggle i {
            color: #6d4c41;
        }
    </style>
</body>
</html>
