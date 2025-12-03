
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ana's Sweet Spot | Artisan Bakery</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <!-- Apple Garamond-style fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,500;1,600&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles - Theme Variables */
        :root {
            /* Light Theme Colors - Apple-inspired */
            --light-bg: #fcfcfc;
            --light-card: #ffffff;
            --light-header: rgba(255, 255, 255, 0.92);
            --light-text: #333333;
            --light-text-secondary: #666666;
            --light-border: rgba(229, 229, 234, 0.8);
            --light-shadow: rgba(0, 0, 0, 0.08);
            
            /* Dark Theme Colors - Apple-inspired */
            --dark-bg: #000000;
            --dark-card: #1c1c1e;
            --dark-header: rgba(28, 28, 30, 0.92);
            --dark-text: #f5f5f7;
            --dark-text-secondary: #98989d;
            --dark-border: #38383a;
            --dark-shadow: rgba(0, 0, 0, 0.3);
            
            /* Brand Colors (Apple-inspired pastel) */
            --soft-pink: #ffdde1;
            --dusty-rose: #e8b4bc;
            --deep-rose: #d48a97;
            --cream: #fefefe;
            --chocolate: #1d1d1f;
            --gold: #d4af37;
            --light-gold: #f5f0e1;
            --accent-dark: #2c2c2e;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        /* Apple Garamond Font Styling */
        body {
            font-family: 'Cormorant Garamond', Garamond, 'Times New Roman', serif;
            font-weight: 400;
            line-height: 1.6;
            letter-spacing: -0.01em;
            overflow-x: hidden;
            transition: all 0.3s ease;
        }
        
        /* Apple-style typography hierarchy */
        h1, h2, h3, h4, .logo {
            font-family: 'Cormorant Garamond', Garamond, 'Times New Roman', serif;
            font-weight: 600;
            letter-spacing: -0.03em;
            line-height: 1.1;
        }
        
        /* Body text for paragraphs, lists, etc. */
        p, li, .form-control, .btn, nav a, .theme-text {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            font-weight: 400;
            letter-spacing: -0.01em;
        }
        
        /* Light Theme (Default) */
        body.light-theme {
            background-color: var(--light-bg);
            color: var(--light-text);
        }
        
        /* Dark Theme */
        body.dark-theme {
            background-color: var(--dark-bg);
            color: var(--dark-text);
        }
        
        .light-theme h1, 
        .light-theme h2, 
        .light-theme h3, 
        .light-theme .logo {
            color: var(--chocolate);
        }
        
        .dark-theme h1, 
        .dark-theme h2, 
        .dark-theme h3, 
        .dark-theme .logo {
            color: var(--gold);
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Background */
        .page-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('https://www.dropbox.com/scl/fi/ofyspzth9gl99x2kk97bh/IMG_7155.jpeg?rlkey=dp20cws62yyci0jpsa65qwx0z&st=pbetxe8a&raw=1');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            z-index: -1;
        }
        
        .light-theme .page-background {
            opacity: 0.4;
            filter: brightness(1.05);
        }
        
        .dark-theme .page-background {
            opacity: 0.2;
            filter: brightness(0.7);
        }
        
        .content-overlay {
            position: relative;
            z-index: 1;
        }
        
        /* Hero Section */
        .hero {
            border-radius: 12px;
            margin: 20px;
            padding: 80px 20px;
            transition: all 0.3s ease;
            text-align: center;
        }
        
        .light-theme .hero {
            background-color: rgba(255, 255, 255, 0.82);
            backdrop-filter: blur(20px);
            box-shadow: 0 8px 32px var(--light-shadow);
            border: 1px solid var(--light-border);
        }
        
        .dark-theme .hero {
            background-color: rgba(28, 28, 30, 0.82);
            backdrop-filter: blur(20px);
            box-shadow: 0 8px 32px var(--dark-shadow);
            border: 1px solid var(--dark-border);
        }
        
        /* Navigation */
        header {
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            padding: 15px 0;
            transition: all 0.3s ease;
        }
        
        .light-theme header {
            background-color: rgba(255, 255, 255, 0.72);
            border-bottom: 1px solid var(--light-border);
        }
        
        .dark-theme header {
            background-color: rgba(28, 28, 30, 0.72);
            border-bottom: 1px solid var(--dark-border);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 2.8rem;
            font-weight: 600;
            letter-spacing: -0.03em;
        }
        
        .light-theme .logo {
            color: var(--chocolate);
        }
        
        .dark-theme .logo {
            color: var(--gold);
        }
        
        .logo span {
            color: var(--deep-rose);
            font-weight: 600;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }
        
        nav a {
            text-decoration: none;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            font-weight: 500;
            font-size: 1rem;
            padding: 8px 16px;
            border-radius: 20px;
            transition: all 0.3s ease;
            position: relative;
        }
        
        .light-theme nav a {
            color: var(--light-text);
        }
        
        .dark-theme nav a {
            color: var(--dark-text);
        }
        
        .light-theme nav a:hover {
            color: var(--deep-rose);
            background-color: rgba(232, 180, 188, 0.08);
        }
        
        .dark-theme nav a:hover {
            color: var(--deep-rose);
            background-color: rgba(212, 138, 151, 0.12);
        }
        
        nav a.active {
            color: var(--deep-rose);
        }
        
        .light-theme nav a.active {
            background-color: rgba(232, 180, 188, 0.1);
        }
        
        .dark-theme nav a.active {
            background-color: rgba(212, 138, 151, 0.15);
        }
        
        nav a.active:after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 50%;
            transform: translateX(-50%);
            width: 3px;
            height: 3px;
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
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Hero Section */
        .hero h1 {
            font-size: 4rem;
            margin-bottom: 20px;
            font-weight: 600;
            letter-spacing: -0.03em;
        }
        
        .light-theme .hero h1 {
            color: var(--chocolate);
        }
        
        .dark-theme .hero h1 {
            color: var(--gold);
        }
        
        .hero p {
            font-size: 1.4rem;
            max-width: 700px;
            margin: 0 auto 40px;
            font-family: 'Cormorant Garamond', Garamond, serif;
            font-style: italic;
            font-weight: 300;
        }
        
        .light-theme .hero p {
            color: var(--light-text-secondary);
        }
        
        .dark-theme .hero p {
            color: var(--dark-text-secondary);
        }
        
        .cta-button {
            display: inline-block;
            background: linear-gradient(135deg, var(--deep-rose), var(--dusty-rose));
            color: white;
            padding: 16px 42px;
            border-radius: 24px;
            text-decoration: none;
            font-size: 1.1rem;
            font-weight: 500;
            font-family: 'Inter', -apple-system, sans-serif;
            box-shadow: 0 4px 20px rgba(212, 138, 151, 0.2);
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            letter-spacing: -0.01em;
        }
        
        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 25px rgba(212, 138, 151, 0.3);
        }
        
        /* Menu Page */
        .page-title {
            text-align: center;
            font-size: 3.2rem;
            margin-bottom: 50px;
            position: relative;
            padding-bottom: 20px;
            font-weight: 600;
        }
        
        .page-title:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 1px;
            background: var(--deep-rose);
        }
        
        .flavors-section {
            margin-bottom: 80px;
        }
        
        .flavors-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }
        
        .flavor-card {
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        
        .light-theme .flavor-card {
            background: var(--light-card);
            box-shadow: 0 4px 24px var(--light-shadow);
            border: 1px solid var(--light-border);
        }
        
        .dark-theme .flavor-card {
            background: var(--dark-card);
            box-shadow: 0 4px 24px var(--dark-shadow);
            border: 1px solid var(--dark-border);
        }
        
        .flavor-card:hover {
            transform: translateY(-8px);
        }
        
        .light-theme .flavor-card:hover {
            box-shadow: 0 12px 32px rgba(0, 0, 0, 0.1);
        }
        
        .dark-theme .flavor-card:hover {
            box-shadow: 0 12px 32px rgba(0, 0, 0, 0.4);
            border-color: var(--deep-rose);
        }
        
        .flavor-content {
            padding: 25px;
        }
        
        .flavor-content h3 {
            font-size: 1.6rem;
            margin-bottom: 12px;
            color: var(--deep-rose);
            font-weight: 600;
        }
        
        .flavor-content p {
            font-family: 'Inter', sans-serif;
            font-size: 0.95rem;
            line-height: 1.5;
        }
        
        .light-theme .flavor-content p {
            color: var(--light-text);
        }
        
        .dark-theme .flavor-content p {
            color: var(--dark-text-secondary);
        }
        
        /* Pricing Section */
        .pricing-section {
            margin-bottom: 80px;
        }
        
        .pricing-category {
            margin-bottom: 50px;
        }
        
        .pricing-category h3 {
            font-size: 2rem;
            margin-bottom: 30px;
            text-align: center;
            font-weight: 600;
        }
        
        .light-theme .pricing-category h3 {
            color: var(--chocolate);
        }
        
        .dark-theme .pricing-category h3 {
            color: var(--chocolate);
        }
        
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 22px;
        }
        
        .price-card {
            border-radius: 12px;
            padding: 28px 22px;
            text-align: center;
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
            height: 2px;
            background: linear-gradient(90deg, var(--dusty-rose), var(--gold));
        }
        
        .light-theme .price-card {
            background: var(--light-card);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.06);
            border: 1px solid rgba(212, 175, 55, 0.1);
        }
        
        .dark-theme .price-card {
            background: var(--dark-card);
            box-shadow: 0 4px 20px var(--dark-shadow);
            border: 1px solid var(--dark-border);
        }
        
        .price-card:hover {
            transform: translateY(-4px);
        }
        
        .light-theme .price-card:hover {
            box-shadow: 0 8px 28px rgba(0, 0, 0, 0.08);
        }
        
        .dark-theme .price-card:hover {
            box-shadow: 0 8px 28px rgba(0, 0, 0, 0.4);
            border-color: var(--gold);
        }
        
        .price-card h4 {
            font-size: 1.3rem;
            margin-bottom: 15px;
            font-weight: 600;
        }
        
        .light-theme .price-card h4 {
            color: var(--chocolate);
        }
        
        .dark-theme .price-card h4 {
            color: var(--dark-text);
        }
        
        .price {
            font-size: 2.2rem;
            color: var(--deep-rose);
            font-weight: 600;
            margin: 15px 0;
            font-family: 'Cormorant Garamond', serif;
        }
        
        .price-image {
            height: 160px;
            background-size: cover;
            background-position: center;
            border-radius: 8px;
            margin-top: 15px;
        }
        
        .light-theme .price-image {
            border: 1px solid var(--light-border);
        }
        
        .dark-theme .price-image {
            border: 1px solid var(--dark-border);
        }
        
        /* Gallery Section */
        .gallery-section {
            margin: 100px 0;
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 22px;
            margin-top: 40px;
        }
        
        .gallery-item {
            border-radius: 12px;
            overflow: hidden;
            height: 280px;
            background-size: cover;
            background-position: center;
            transition: all 0.3s ease;
            position: relative;
            cursor: pointer;
        }
        
        .dark-theme .gallery-item {
            border: 1px solid rgba(255, 255, 255, 0.05);
        }
        
        .gallery-item:hover {
            transform: scale(1.02);
        }
        
        .dark-theme .gallery-item:hover {
            border-color: var(--deep-rose);
        }
        
        /* Policies Section */
        .policies-section {
            margin: 100px 0;
            border-radius: 12px;
            padding: 50px;
            backdrop-filter: blur(20px);
        }
        
        .light-theme .policies-section {
            background-color: rgba(255, 255, 255, 0.72);
            border: 1px solid var(--light-border);
        }
        
        .dark-theme .policies-section {
            background-color: rgba(28, 28, 30, 0.72);
            border: 1px solid var(--dark-border);
        }
        
        .policy-box {
            border-radius: 12px;
            padding: 30px;
            margin: 30px 0;
            border-left: 3px solid var(--deep-rose);
        }
        
        .light-theme .policy-box {
            background: var(--light-card);
        }
        
        .dark-theme .policy-box {
            background: rgba(40, 40, 40, 0.6);
        }
        
        .policy-box h3 {
            color: var(--deep-rose);
            margin-bottom: 20px;
            font-size: 1.6rem;
            font-weight: 600;
        }
        
        .policy-box ul {
            padding-left: 20px;
            margin-bottom: 15px;
        }
        
        .light-theme .policy-box li {
            color: var(--light-text);
        }
        
        .dark-theme .policy-box li {
            color: var(--dark-text-secondary);
        }
        
        .policy-box li {
            margin-bottom: 12px;
            font-family: 'Inter', sans-serif;
            font-size: 0.95rem;
        }
        
        .warning {
            padding: 18px;
            margin: 20px 0;
            border-radius: 8px;
        }
        
        .light-theme .warning {
            background-color: rgba(255, 193, 7, 0.08);
            border-left: 3px solid #ffc107;
            color: var(--light-text);
        }
        
        .dark-theme .warning {
            background-color: rgba(255, 193, 7, 0.08);
            border-left: 3px solid #ffc107;
            color: var(--dark-text);
        }
        
        /* Order Form - Multi Step */
        .order-container {
            max-width: 800px;
            margin: 0 auto;
            border-radius: 12px;
            overflow: hidden;
        }
        
        .light-theme .order-container {
            background: var(--light-card);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
            border: 1px solid var(--light-border);
        }
        
        .dark-theme .order-container {
            background: var(--dark-card);
            box-shadow: 0 8px 32px var(--dark-shadow);
            border: 1px solid var(--dark-border);
        }
        
        .form-header {
            background: linear-gradient(135deg, var(--deep-rose), var(--dusty-rose));
            color: white;
            padding: 25px;
            text-align: center;
        }
        
        .form-header h2 {
            color: white;
            font-size: 2.2rem;
            margin-bottom: 10px;
            font-weight: 600;
        }
        
        .step-indicator {
            display: flex;
            justify-content: center;
            margin-top: 20px;
            gap: 25px;
        }
        
        .step {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 500;
            transition: all 0.3s ease;
            color: white;
            font-family: 'Inter', sans-serif;
            font-size: 0.9rem;
        }
        
        .step.active {
            background-color: white;
            color: var(--deep-rose);
        }
        
        .step.completed {
            background-color: var(--light-gold);
            color: var(--chocolate);
        }
        
        .form-body {
            padding: 40px;
        }
        
        .form-step {
            display: none;
            animation: fadeIn 0.4s ease;
        }
        
        .form-step.active {
            display: block;
        }
        
        .step-title {
            font-size: 1.8rem;
            margin-bottom: 25px;
            text-align: center;
            font-weight: 600;
        }
        
        .light-theme .step-title {
            color: var(--chocolate);
        }
        
        .dark-theme .step-title {
            color: var(--gold);
        }
        
        .flavor-options, .size-options {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 18px;
            margin-top: 20px;
        }
        
        .option-card {
            border-radius: 10px;
            padding: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: center;
        }
        
        .light-theme .option-card {
            border: 1px solid var(--light-border);
            color: var(--light-text);
        }
        
        .dark-theme .option-card {
            border: 1px solid var(--dark-border);
            background: rgba(40, 40, 40, 0.5);
            color: var(--dark-text-secondary);
        }
        
        .light-theme .option-card:hover {
            border-color: var(--dusty-rose);
            background-color: rgba(232, 180, 188, 0.03);
        }
        
        .dark-theme .option-card:hover {
            border-color: var(--dusty-rose);
            background-color: rgba(232, 180, 188, 0.08);
            color: var(--dark-text);
        }
        
        .option-card.selected {
            border-color: var(--deep-rose);
        }
        
        .light-theme .option-card.selected {
            background-color: rgba(232, 180, 188, 0.06);
        }
        
        .dark-theme .option-card.selected {
            background-color: rgba(232, 180, 188, 0.12);
            color: var(--dark-text);
        }
        
        .option-card h4 {
            font-size: 1.2rem;
            margin-bottom: 10px;
            font-weight: 600;
        }
        
        .light-theme .option-card h4 {
            color: var(--chocolate);
        }
        
        .dark-theme .option-card h4 {
            color: var(--chocolate);
        }
        
        .upload-area {
            border: 1px dashed var(--dusty-rose);
            border-radius: 12px;
            padding: 40px 20px;
            text-align: center;
            margin: 30px 0;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .light-theme .upload-area {
            background: rgba(255, 255, 255, 0.5);
        }
        
        .dark-theme .upload-area {
            background: rgba(40, 40, 40, 0.3);
        }
        
        .upload-area:hover {
            border-color: var(--deep-rose);
            background-color: rgba(232, 180, 188, 0.03);
        }
        
        .upload-icon {
            font-size: 2.5rem;
            color: var(--dusty-rose);
            margin-bottom: 15px;
        }
        
        .skip-button {
            background: none;
            border: none;
            color: var(--deep-rose);
            text-decoration: underline;
            cursor: pointer;
            font-size: 0.95rem;
            margin-top: 15px;
            font-family: 'Inter', sans-serif;
        }
        
        .terms-box {
            border-radius: 10px;
            padding: 22px;
            margin: 30px 0;
            max-height: 280px;
            overflow-y: auto;
        }
        
        .light-theme .terms-box {
            border: 1px solid rgba(232, 180, 188, 0.3);
            background-color: rgba(250, 250, 250, 0.5);
            color: var(--light-text);
        }
        
        .dark-theme .terms-box {
            border: 1px solid rgba(232, 180, 188, 0.2);
            background-color: rgba(30, 30, 30, 0.6);
            color: var(--dark-text-secondary);
        }
        
        .terms-box h4 {
            color: var(--deep-rose);
            margin-bottom: 15px;
            font-size: 1.2rem;
            font-weight: 600;
        }
        
        .terms-box ul {
            padding-left: 20px;
            margin-bottom: 15px;
        }
        
        .terms-box li {
            margin-bottom: 10px;
            font-family: 'Inter', sans-serif;
            font-size: 0.9rem;
        }
        
        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-top: 20px;
        }
        
        .light-theme .checkbox-group {
            color: var(--light-text);
        }
        
        .dark-theme .checkbox-group {
            color: var(--dark-text-secondary);
        }
        
        .form-control {
            width: 100%;
            padding: 14px;
            border-radius: 8px;
            font-size: 0.95rem;
            font-family: 'Inter', sans-serif;
            margin-bottom: 20px;
            transition: all 0.3s ease;
            letter-spacing: -0.01em;
        }
        
        .light-theme .form-control {
            border: 1px solid var(--light-border);
            background-color: white;
            color: var(--light-text);
        }
        
        .dark-theme .form-control {
            border: 1px solid var(--dark-border);
            background-color: rgba(40, 40, 40, 0.7);
            color: var(--dark-text);
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--deep-rose);
        }
        
        .form-navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 40px;
            padding-top: 30px;
        }
        
        .light-theme .form-navigation {
            border-top: 1px solid var(--light-border);
        }
        
        .dark-theme .form-navigation {
            border-top: 1px solid var(--dark-border);
        }
        
        .btn {
            padding: 12px 28px;
            border-radius: 20px;
            font-size: 0.95rem;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s ease;
            font-family: 'Inter', sans-serif;
            border: none;
            letter-spacing: -0.01em;
        }
        
        .btn-prev {
            color: var(--deep-rose);
        }
        
        .light-theme .btn-prev {
            background-color: white;
            border: 1px solid var(--light-border);
        }
        
        .dark-theme .btn-prev {
            background-color: rgba(40, 40, 40, 0.8);
            border: 1px solid var(--dark-border);
        }
        
        .btn-next, .btn-submit {
            background: linear-gradient(135deg, var(--deep-rose), var(--dusty-rose));
            color: white;
        }
        
        .light-theme .btn-prev:hover {
            background-color: rgba(232, 180, 188, 0.08);
        }
        
        .dark-theme .btn-prev:hover {
            background-color: rgba(232, 180, 188, 0.15);
            border-color: var(--dusty-rose);
        }
        
        .btn-next:hover, .btn-submit:hover {
            transform: translateY(-2px);
        }
        
        .btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
            transform: none !important;
        }
        
        /* Footer */
        footer {
            padding: 40px 0 20px;
            text-align: center;
        }
        
        .light-theme footer {
            background-color: var(--light-bg);
            border-top: 1px solid var(--light-border);
        }
        
        .dark-theme footer {
            background-color: var(--dark-bg);
            border-top: 1px solid var(--dark-border);
        }
        
        .footer-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .footer-logo {
            font-size: 2.2rem;
            margin-bottom: 20px;
            font-weight: 600;
        }
        
        .light-theme .footer-logo {
            color: var(--deep-rose);
        }
        
        .dark-theme .footer-logo {
            color: var(--gold);
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 25px 0;
        }
        
        .social-icons a {
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }
        
        .light-theme .social-icons a {
            color: var(--chocolate);
        }
        
        .dark-theme .social-icons a {
            color: var(--dark-text);
        }
        
        .social-icons a:hover {
            color: var(--deep-rose);
            transform: translateY(-2px);
        }
        
        .copyright {
            margin-top: 30px;
            padding-top: 20px;
            font-size: 0.85rem;
        }
        
        .light-theme .copyright {
            border-top: 1px solid var(--light-border);
            color: #888;
        }
        
        .dark-theme .copyright {
            border-top: 1px solid var(--dark-border);
            color: var(--dark-text-secondary);
        }
        
        /* Theme Toggle Button */
        .theme-toggle {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 48px;
            height: 48px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            z-index: 1001;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }
        
        .light-theme .theme-toggle {
            background-color: rgba(255, 255, 255, 0.8);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            border: 1px solid var(--light-border);
        }
        
        .dark-theme .theme-toggle {
            background-color: rgba(40, 40, 40, 0.8);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            border: 1px solid var(--dark-border);
        }
        
        .theme-toggle:hover {
            transform: scale(1.08);
        }
        
        .theme-toggle i {
            font-size: 1.3rem;
        }
        
        .light-theme .theme-toggle i {
            color: var(--chocolate);
        }
        
        .dark-theme .theme-toggle i {
            color: var(--gold);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 15px;
            }
            
            nav ul {
                gap: 12px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .page-title {
                font-size: 2.4rem;
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
                padding: 60px 20px;
            }
            
            .logo {
                font-size: 2.4rem;
            }
        }
        
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .logo {
                font-size: 2rem;
            }
            
            .page-title {
                font-size: 2rem;
            }
            
            .form-navigation {
                flex-direction: column;
                gap: 12px;
            }
            
            .btn {
                width: 100%;
            }
            
            .theme-toggle {
                bottom: 15px;
                right: 15px;
                width: 42px;
                height: 42px;
            }
        }
    </style>
</head>
<body class="light-theme">
    <!-- Background -->
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
                    <h2 style="font-size: 2.4rem; margin-bottom: 30px; font-weight: 600;">Why Choose Us</h2>
                    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 40px; margin-top: 40px;">
                        <div>
                            <div style="font-size: 2.5rem; color: var(--deep-rose); margin-bottom: 15px;">🎂</div>
                            <h3 style="font-size: 1.6rem; font-weight: 600;">Custom Designs</h3>
                            <p class="theme-text">Each cake is uniquely crafted to match your vision and occasion.</p>
                        </div>
                        <div>
                            <div style="font-size: 2.5rem; color: var(--deep-rose); margin-bottom: 15px;">👩‍🍳</div>
                            <h3 style="font-size: 1.6rem; font-weight: 600;">Artisan Quality</h3>
                            <p class="theme-text">Made from scratch with premium ingredients and attention to detail.</p>
                        </div>
                        <div>
                            <div style="font-size: 2.5rem; color: var(--deep-rose); margin-bottom: 15px;">💝</div>
                            <h3 style="font-size: 1.6rem; font-weight: 600;">Made with Love</h3>
                            <p class="theme-text">Every creation is infused with care and passion for the craft.</p>
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
                    <p style="text-align: center; font-size: 1.1rem; max-width: 800px; margin: 0 auto 50px; font-family: 'Cormorant Garamond', serif;" class="theme-text">
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
                            <li>NO CHANGES CAN BE MADE TO YOUR ORDER ONCE DEPOSIT IS SENT!</li>
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
                                <p style="text-align: center; margin-bottom: 30px; font-family: 'Cormorant Garamond', serif;" class="theme-text">Select your favorite cake flavor from our artisan collection</p>
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
                                <p style="text-align: center; margin-bottom: 30px; font-family: 'Cormorant Garamond', serif;" class="theme-text">Choose the perfect size and shape for your occasion</p>
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
                                <p style="text-align: center; margin-bottom: 30px; font-family: 'Cormorant Garamond', serif;" class="theme-text">Help us visualize your dream cake (optional)</p>
                                
                                <div class="upload-area" id="uploadArea">
                                    <div class="upload-icon">
                                        <i class="fas fa-cloud-upload-alt"></i>
                                    </div>
                                    <h4>Upload Inspiration Photos</h4>
                                    <p>Click to browse photos from your device</p>
                                    <p style="font-size: 0.9rem; margin-top: 10px;" class="theme-text">Max 5 images, 5MB each</p>
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
                                <p style="text-align: center; margin-bottom: 30px; font-family: 'Cormorant Garamond', serif;" class="theme-text">Please review our policies before proceeding</p>
                                
                                <div class="terms-box">
                                    <h4>Ordering Policies</h4>
                                    <ul>
                                        <li>A 50% non-refundable deposit is required at time of booking</li>
                                        <li>Remaining balance must be paid prior to pickup or cash only at pickup</li>
                                        <li>No changes can be made to your order once deposit is sent</li>
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
                                <p style="text-align: center; margin-bottom: 30px; font-family: 'Cormorant Garamond', serif;" class="theme-text">We'll contact you to confirm details and request deposit</p>
                                
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
                                    <small style="display: block; margin-top: 5px;" class="theme-text">Please allow 3-5 days for custom orders</small>
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
                <p style="max-width: 600px; margin: 0 auto 20px; font-family: 'Cormorant Garamond', serif;" class="theme-text">Creating beautiful, delicious custom cakes for all your special occasions.</p>
                
                <div class="social-icons">
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-facebook"></i></a>
                    <a href="#"><i class="fab fa-tiktok"></i></a>
                    <a href="#"><i class="fas fa-envelope"></i></a>
                </div>
                
                <div style="margin-top: 20px;" class="theme-text">
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
                    <p style="margin-bottom: 10px;" class="theme-text">${cupcake.description}</p>
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
                    <p style="font-size: 0.9rem;" class="theme-text">${flavor.description}</p>
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
                    <div style="color: var(--deep-rose); font-weight: 600; margin: 10px 0;">${cake.price}</div>
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
                    <div style="color: var(--deep-rose); font-weight: 600; margin: 10px 0;">${cupcake.price}</div>
                    <p style="font-size: 0.9rem;" class="theme-text">${cupcake.description}</p>
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
                        img.style.border = '1px solid var(--dusty-rose)';
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
                    document.body.classList.add('dark-theme');
                    themeIcon.className = 'fas fa-sun';
                    localStorage.setItem('theme', 'dark');
                } else {
                    // Switch to light theme
                    document.body.classList.remove('dark-theme');
                    document.body.classList.add('light-theme');
                    themeIcon.className = 'fas fa-moon';
                    localStorage.setItem('theme', 'light');
                }
            });
            
            // Check for saved theme preference
            const savedTheme = localStorage.getItem('theme');
            if (savedTheme === 'dark') {
                document.body.classList.remove('light-theme');
                document.body.classList.add('dark-theme');
                themeIcon.className = 'fas fa-sun';
            }
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
</body>
</html>
