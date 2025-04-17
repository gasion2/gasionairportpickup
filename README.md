<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gasion Airport Transfers | Reliable Pickups in Uganda</title>
    <meta name="description" content="Professional airport transfers, wedding transport, and corporate travel services in Uganda. Book your ride today!">

    <!-- Preload critical resources -->
    <link rel="preload" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" as="style">
    <link rel="preload" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" as="style">
    <link rel="preload" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js" as="script">

    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

    <!-- Leaflet CSS -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css">

    <!-- Placeholder for Flutterwave (uncomment when integrating) -->
    <!-- <script src="https://checkout.flutterwave.com/v3.js"></script> -->

    <style>
        /* ===== Core Styles ===== */
        :root {
            --primary: #FF6B01;  /* Brand orange */
            --primary-dark: #E05D00;
            --secondary: #003580; /* Navy blue */
            --accent: #FFC107;    /* Gold */
            --light: #F5F5F5;
            --dark: #333333;
            --gray: #777777;
            --success: #28a745;
            --danger: #dc3545;
            --shadow: 0 4px 12px rgba(0,0,0,0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Roboto', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
            overflow-x: hidden;
        }

        html {
            scroll-behavior: smooth;
        }

        img, video {
            max-width: 100%;
            height: auto;
        }

        /* ===== Utility Classes ===== */
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .btn {
            display: inline-block;
            padding: 12px 24px;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 4px;
            font-weight: 600;
            text-decoration: none;
            cursor: pointer;
            transition: var(--transition);
        }

        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: var(--shadow);
        }

        .btn-block {
            display: block;
            width: 100%;
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
            color: var(--secondary);
        }

        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: var(--primary);
            margin: 12px auto 0;
        }

        /* ===== Header ===== */
        header {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
                        url('https://images.unsplash.com/photo-1556388158-158ea5ccacbd?ixlib=rb-1.2.1&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 40px 0;
            text-align: center;
            position: relative;
        }

        .header-content {
            position: relative;
            z-index: 2;
        }

        .logo {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 10px;
            color: var(--accent);
        }

        .tagline {
            font-size: 1.2rem;
            margin-bottom: 25px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .safety-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background: rgba(255,255,255,0.9);
            color: var(--secondary);
            padding: 6px 12px;
            border-radius: 16px;
            font-size: 0.8rem;
            font-weight: 600;
            display: flex;
            align-items: center;
        }

        .safety-badge i {
            margin-right: 6px;
            color: var(--primary);
            font-size: 0.9rem;
        }

        /* ===== Contact Bar ===== */
        .contact-bar {
            background-color: var(--secondary);
            padding: 15px 0;
        }

        .contact-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
        }

        .contact-item {
            display: flex;
            align-items: center;
            color: white;
            margin: 5px 0;
        }

        .contact-item i {
            margin-right: 10px;
            color: var(--accent);
            font-size: 1.1rem;
        }

        /* ===== Promo Banner ===== */
        .promo-banner {
            background-color: var(--accent);
            color: var(--secondary);
            padding: 12px 0;
            text-align: center;
            font-weight: 600;
        }

        /* ===== Navigation ===== */
        nav {
            background-color: var(--primary);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .nav-logo {
            color: white;
            font-weight: 700;
            font-size: 1.3rem;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 20px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 8px 12px;
            border-radius: 4px;
            transition: var(--transition);
        }

        .nav-links a:hover {
            background-color: rgba(255,255,255,0.2);
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* ===== Trust Badges ===== */
        .trust-badges {
            padding: 30px 0;
            background-color: white;
        }

        .badges-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
        }

        .badge {
            height: 60px;
            width: auto;
            object-fit: contain;
            filter: grayscale(100%);
            opacity: 0.7;
            transition: var(--transition);
        }

        .badge:hover {
            filter: grayscale(0);
            opacity: 1;
        }

        /* ===== Services Section ===== */
        .services {
            padding: 60px 0;
            background-color: var(--light);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }

        .service-img {
            height: 200px;
            overflow: hidden;
        }

        .service-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .service-card:hover .service-img img {
            transform: scale(1.05);
        }

        .service-content {
            padding: 20px;
        }

        .service-content h3 {
            color: var(--secondary);
            margin-bottom: 10px;
            font-size: 1.3rem;
        }

        /* ===== Testimonials ===== */
        .testimonials {
            padding: 60px 0;
            background-color: white;
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .testimonial {
            background: var(--light);
            padding: 25px;
            border-radius: 8px;
            box-shadow: var(--shadow);
        }

        .testimonial-header {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .testimonial-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 15px;
        }

        .testimonial-name {
            font-weight: 600;
            color: var(--secondary);
        }

        .testimonial-location {
            color: var(--gray);
            font-size: 0.9rem;
        }

        .testimonial-text {
            font-style: italic;
            margin-bottom: 15px;
        }

        .testimonial-rating {
            color: var(--accent);
        }

        /* ===== Booking Section ===== */
        .booking {
            padding: 60px 0;
            background-color: var(--light);
        }

        .booking-container {
            display: grid;
            grid-template-columns: 1fr;
            gap: 40px;
        }

        .booking-form {
            background-color: white;
            border-radius: 8px;
            padding: 30px;
            box-shadow: var(--shadow);
            position: relative;
        }

        .loyalty-badge {
            position: absolute;
            top: -15px;
            right: 20px;
            background-color: var(--accent);
            color: var(--secondary);
            padding: 8px 16px;
            border-radius: 20px;
            font-weight: 600;
            display: flex;
            align-items: center;
        }

        .loyalty-badge i {
            margin-right: 8px;
        }

        .quick-locations {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }

        .location-btn {
            background: var(--light);
            border: 1px solid var(--primary);
            color: var(--primary);
            padding: 8px 16px;
            border-radius: 4px;
            font-size: 0.9rem;
            cursor: pointer;
            transition: var(--transition);
        }

        .location-btn:hover {
            background: var(--primary);
            color: white;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--secondary);
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-control:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(255,107,1,0.2);
        }

        .form-row {
            display: flex;
            gap: 20px;
        }

        .form-row .form-group {
            flex: 1;
        }

        #map {
            height: 300px;
            width: 100%;
            border-radius: 8px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
        }

        .distance-info {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
            display: none;
        }

        .distance-info p {
            margin-bottom: 8px;
            display: flex;
            justify-content: space-between;
        }

        .distance-info span:last-child {
            font-weight: 600;
            color: var(--secondary);
        }

        /* ===== Payment Modal ===== */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            z-index: 2000;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .modal-content {
            background-color: white;
            border-radius: 8px;
            width: 100%;
            max-width: 500px;
            padding: 30px;
            position: relative;
            animation: modalFadeIn 0.3s ease;
            max-height: 90vh;
            overflow-y: auto;
        }

        @keyframes modalFadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--gray);
            transition: var(--transition);
        }

        .close-modal:hover {
            color: var(--dark);
        }

        .modal-title {
            margin-bottom: 20px;
            color: var(--secondary);
        }

        .booking-summary {
            margin-bottom: 25px;
        }

        .summary-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        .summary-item:last-child {
            font-weight: 600;
            color: var(--secondary);
            margin-top: 12px;
            padding-top: 12px;
            border-top: 1px solid #eee;
        }

        .payment-options {
            margin: 25px 0;
        }

        .payment-option {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            cursor: pointer;
            transition: var(--transition);
        }

        .payment-option:hover {
            border-color: var(--primary);
        }

        .payment-option input {
            margin-right: 15px;
        }

        .payment-option-label {
            font-weight: 600;
        }

        .payment-form {
            display: none;
            margin-top: 15px;
            animation: fadeIn 0.3s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .payment-form.active {
            display: block;
        }

        /* ===== WhatsApp Float ===== */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #25D366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.8rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
            z-index: 1000;
            transition: var(--transition);
            text-decoration: none;
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 16px rgba(0,0,0,0.3);
        }

        /* ===== Footer ===== */
        footer {
            background-color: var(--secondary);
            color: white;
            padding: 60px 0 30px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            color: var(--accent);
            margin-bottom: 20px;
            font-size: 1.2rem;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: white;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--accent);
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            color: white;
            font-size: 1.3rem;
            transition: var(--transition);
        }

        .social-links a:hover {
            color: var(--accent);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: rgba(255,255,255,0.7);
            font-size: 0.9rem;
        }

        /* ===== Robo-Gasion Chatbot Styles ===== */
        .robo-container {
            position: fixed;
            bottom: 100px;
            right: 30px;
            z-index: 1000;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        .robo-toggle {
            width: 60px;
            height: 60px;
            background-color: var(--primary);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
        }

        .robo-toggle:hover {
            transform: scale(1.1);
        }

        .robo-toggle i {
            color: white;
            font-size: 1.8rem;
            animation: float 3s ease-in-out infinite;
        }

        .robo-chatbox {
            width: 350px;
            height: 500px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 5px 30px rgba(0,0,0,0.2);
            overflow: hidden;
            display: none;
            flex-direction: column;
            transform: translateY(20px);
            opacity: 0;
            transition: all 0.3s ease;
        }

        .robo-chatbox.active {
            display: flex;
            transform: translateY(0);
            opacity: 1;
        }

        .robo-header {
            background-color: var(--primary);
            color: white;
            padding: 15px;
            display: flex;
            align-items: center;
        }

        .robo-header img {
            width: 40px;
            height: 40px;
            margin-right: 10px;
            border-radius: 50%;
        }

        .robo-header h3 {
            margin: 0;
            font-size: 1.1rem;
        }

        .robo-close {
            margin-left: auto;
            cursor: pointer;
            font-size: 1.2rem;
        }

        .robo-messages {
            flex: 1;
            padding: 15px;
            overflow-y: auto;
            background-color: #f9f9f9;
        }

        .message {
            margin-bottom: 15px;
            max-width: 80%;
            padding: 10px 15px;
            border-radius: 18px;
            line-height: 1.4;
            font-size: 0.95rem;
            position: relative;
        }

        .bot-message {
            background-color: white;
            color: var(--dark);
            border: 1px solid #eee;
            border-top-left-radius: 5px;
            align-self: flex-start;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }

        .user-message {
            background-color: var(--primary);
            color: white;
            border-top-right-radius: 5px;
            align-self: flex-end;
            margin-left: auto;
        }

        .robo-input {
            display: flex;
            padding: 15px;
            border-top: 1px solid #eee;
            background-color: white;
        }

        .robo-input input {
            flex: 1;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 30px;
            outline: none;
            font-size: 0.95rem;
        }

        .robo-input button {
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 50%;
            width: 45px;
            height: 45px;
            margin-left: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .robo-input button:hover {
            background-color: var(--primary-dark);
        }

        .quick-replies {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 10px;
        }

        .quick-reply {
            background-color: white;
            border: 1px solid var(--primary);
            color: var(--primary);
            padding: 6px 12px;
            border-radius: 15px;
            font-size: 0.8rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .quick-reply:hover {
            background-color: var(--primary);
            color: white;
        }

        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-5px); }
            100% { transform: translateY(0); }
        }

        /* Luganda language toggle */
        .language-toggle {
            position: absolute;
            top: 10px;
            right: 10px;
            background: rgba(255,255,255,0.9);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            cursor: pointer;
            z-index: 2;
        }

        /* ===== Media Section ===== */
        .media {
            padding: 60px 0;
            background-color: white;
        }

        .video-player {
            background: var(--light);
            border-radius: 8px;
            padding: 20px;
            box-shadow: var(--shadow);
            max-width: 600px;
            margin: 0 auto;
        }

        .video-player video {
            width: 100%;
            border-radius: 8px;
            margin-bottom: 15px;
        }

        .video-controls {
            display: flex;
            gap: 10px;
            justify-content: center;
        }

        .video-controls button {
            background: var(--primary);
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 4px;
            cursor: pointer;
            transition: var(--transition);
        }

        .video-controls button:hover {
            background: var(--primary-dark);
        }

        /* ===== Responsive Styles ===== */
        @media (max-width: 992px) {
            .nav-links {
                display: none;
                width: 100%;
                flex-direction: column;
                margin-top: 20px;
            }

            .nav-links.active {
                display: flex;
            }

            .nav-links li {
                margin: 10px 0;
                margin-left: 0;
            }

            .mobile-menu-btn {
                display: block;
            }

            .form-row {
                flex-direction: column;
                gap: 0;
            }
        }

        @media (max-width: 768px) {
            .header-content {
                padding: 0 20px;
            }

            .logo {
                font-size: 2rem;
            }

            .safety-badge {
                position: static;
                margin: 10px auto;
                width: fit-content;
            }

            .contact-container {
                flex-direction: column;
                align-items: center;
            }

            .contact-item {
                margin: 8px 0;
            }

            .whatsapp-float {
                bottom: 20px;
                right: 20px;
                width: 50px;
                height: 50px;
                font-size: 1.5rem;
            }
        }

        @media (max-width: 576px) {
            .booking-form {
                padding: 20px;
            }

            .modal-content {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- ===== Header ===== -->
    <header>
        <div class="header-content">
            <div class="safety-badge">
                <i class="fas fa-shield-virus"></i> Sanitized Vehicles • Mask Required
            </div>
            <h1 class="logo">Gasion</h1>
            <p class="tagline">Premium Airport Pick-ups & Drop-offs in Uganda</p>
            <a href="#booking" class="btn">Book Your Ride Now</a>
        </div>
    </header>

    <!-- ===== Promo Banner ===== -->
    <div class="promo-banner">
        🚖 <strong>SPECIAL OFFER:</strong> 15% OFF Entebbe Airport transfers booked 24h in advance!
    </div>

    <!-- ===== Contact Bar ===== -->
    <div class="contact-bar">
        <div class="container contact-container">
            <div class="contact-item">
                <i class="fas fa-phone"></i>
                <span>+256 702 201096</span>
            </div>
            <div class="contact-item">
                <i class="fas fa-envelope"></i>
                <span><a href="mailto:info@gasiontransfers.com">info@gasiontransfers.com</a></span>
            </div>
            <div class="contact-item">
                <i class="fas fa-map-marker-alt"></i>
                <span>Kampala, Uganda</span>
            </div>
            <div class="contact-item">
                <i class="fas fa-clock"></i>
                <span>24/7 Service</span>
            </div>
        </div>
    </div>

    <!-- ===== Navigation ===== -->
    <nav>
        <div class="container nav-container">
            <a href="#" class="nav-logo">Gasion</a>
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#booking">Book Now</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- ===== Trust Badges ===== -->
    <div class="trust-badges">
        <div class="container badges-container">
            <img src="https://upload.wikimedia.org/wikipedia/en/thumb/3/3b/Uganda_Tourism_Board_logo.svg/1200px-Uganda_Tourism_Board_logo.svg.png" alt="Uganda Tourism Board Certified" class="badge">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e3/Safe_Travels_Stamp.svg/1200px-Safe_Travels_Stamp.svg.png" alt="Safe Travels Certified" class="badge">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a3/UTB_logo.svg/1200px-UTB_logo.svg.png" alt="Uganda Transport Board" class="badge">
        </div>
    </div>

    <!-- ===== Services Section ===== -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Our Services</h2>
            <div class="services-grid">
                <!-- Service 1 -->
                <div class="service-card">
                    <div class="service-img">
                        <img src="https://images.unsplash.com/photo-1556388158-158ea5ccacbd?ixlib=rb-1.2.1&auto=format&fit=crop&w=2070&q=80" alt="Airport Transfer" loading="lazy">
                    </div>
                    <div class="service-content">
                        <h3>Airport Transfers</h3>
                        <p>Reliable pick-up and drop-off services to/from Entebbe International Airport and all major airports in Uganda.</p>
                        <a href="#booking" class="btn">Book Now</a>
                    </div>
                </div>

                <!-- Service 2 -->
                <div class="service-card">
                    <div class="service-img">
                        <img src="https://images.unsplash.com/photo-1519671482749-fd09be7ccebf?ixlib=rb-1.2.1&auto=format&fit=crop&w=2070&q=80" alt="Wedding Transportation" loading="lazy">
                    </div>
                    <div class="service-content">
                        <h3>Wedding Transportation</h3>
                        <p>Elegant and spacious vehicles for your wedding party, ensuring you arrive in style on your special day.</p>
                        <a href="#booking" class="btn">Book Now</a>
                    </div>
                </div>

                <!-- Service 3 -->
                <div class="service-card">
                    <div class="service-img">
                        <img src="https://images.unsplash.com/photo-1530103862676-de8c9debad1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=2070&q=80" alt="Corporate Events" loading="lazy">
                    </div>
                    <div class="service-content">
                        <h3>Corporate Events</h3>
                        <p>Professional transportation services for business meetings, conferences, and corporate events throughout Uganda.</p>
                        <a href="#booking" class="btn">Book Now</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== Testimonials Section ===== -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <h2 class="section-title">What Our Clients Say</h2>
            <div class="testimonials-grid">
                <!-- Testimonial 1 -->
                <div class="testimonial">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Sarah K." class="testimonial-img" loading="lazy">
                        <div>
                            <div class="testimonial-name">Sarah K.</div>
                            <div class="testimonial-location">Kampala</div>
                        </div>
                    </div>
                    <p class="testimonial-text">"The driver was waiting exactly where promised at Entebbe Airport. Made my arrival so stress-free!"</p>
                    <div class="testimonial-rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                </div>

                <!-- Testimonial 2 -->
                <div class="testimonial">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="James M." class="testimonial-img" loading="lazy">
                        <div>
                            <div class="testimonial-name">James M.</div>
                            <div class="testimonial-location">Entebbe</div>
                        </div>
                    </div>
                    <p class="testimonial-text">"Used Gasion for our wedding transport - flawless service and beautiful vehicles that matched our theme perfectly."</p>
                    <div class="testimonial-rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                </div>

                <!-- Testimonial 3 -->
                <div class="testimonial">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Naomi T." class="testimonial-img" loading="lazy">
                        <div>
                            <div class="testimonial-name">Naomi T.</div>
                            <div class="testimonial-location">Nairobi</div>
                        </div>
                    </div>
                    <p class="testimonial-text">"As a solo female traveler, I felt completely safe with their professional drivers. Will definitely use them again!"</p>
                    <div class="testimonial-rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== Booking Section ===== -->
    <section class="booking" id="booking">
        <div class="container">
            <h2 class="section-title">Book Your Ride</h2>
            <div class="booking-container">
                <div class="booking-form">
                    <div class="loyalty-badge">
                        <i class="fas fa-crown"></i> Earn Free Rides!
                    </div>

                    <form id="transportForm">
                        <div class="quick-locations">
                            <button type="button" class="location-btn" onclick="setLocation('pickup', 'Entebbe International Airport')">
                                <i class="fas fa-plane"></i> From Airport
                            </button>
                            <button type="button" class="location-btn" onclick="setLocation('destination', 'Kampala City Center')">
                                <i class="fas fa-city"></i> To Kampala
                            </button>
                            <button type="button" class="location-btn" onclick="setLocation('pickup', 'Kampala City Center')">
                                <i class="fas fa-city"></i> From Kampala
                            </button>
                            <button type="button" class="location-btn" onclick="setLocation('destination', 'Entebbe International Airport')">
                                <i class="fas fa-plane"></i> To Airport
                            </button>
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label for="fullName" class="form-label">Full Name</label>
                                <input type="text" id="fullName" class="form-control" required>
                            </div>
                            <div class="form-group">
                                <label for="phone" class="form-label">Phone Number</label>
                                <input type="tel" id="phone" class="form-control" required>
                                <small id="phoneError" style="color: var(--danger); display: none;">Please enter a valid Ugandan number (e.g. 0702201096 or 256702201096)</small>
                            </div>
                        </div>

                        <div class="form-group">
                            <label for="email" class="form-label">Email Address</label>
                            <input type="email" id="email" class="form-control">
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label for="serviceType" class="form-label">Service Type</label>
                                <select id="serviceType" class="form-control" required>
                                    <option value="">Select service</option>
                                    <option value="airport">Airport Transfer</option>
                                    <option value="wedding">Wedding</option>
                                    <option value="corporate">Corporate Event</option>
                                    <option value="tour">City Tour</option>
                                    <option value="special">Special Occasion</option>
                                    <option value="long">Long Distance</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="passengers" class="form-label">Passengers</label>
                                <input type="number" id="passengers" class="form-control" min="1" value="1" required>
                            </div>
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label for="pickupDate" class="form-label">Pickup Date</label>
                                <input type="date" id="pickupDate" class="form-control" required>
                            </div>
                            <div class="form-group">
                                <label for="pickupTime" class="form-label">Pickup Time</label>
                                <input type="time" id="pickupTime" class="form-control" required>
                            </div>
                        </div>

                        <div class="form-group">
                            <label for="pickupLocation" class="form-label">Pickup Location</label>
                            <input type="text" id="pickupLocation" class="form-control" placeholder="Enter address or landmark" required>
                            <button type="button" class="location-btn" onclick="toggleMarkerSetting('pickup')">
                                <i class="fas fa-map-marker-alt"></i> Set on Map
                            </button>
                        </div>

                        <div class="form-group">
                            <label for="destination" class="form-label">Destination</label>
                            <input type="text" id="destination" class="form-control" placeholder="Enter address or landmark" required>
                            <button type="button" class="location-btn" onclick="toggleMarkerSetting('destination')">
                                <i class="fas fa-map-marker-alt"></i> Set on Map
                            </button>
                        </div>

                        <div class="form-group">
                            <label class="form-label">Route Map</label>
                            <div id="map"></div>
                            <div class="distance-info" id="distanceInfo">
                                <p>
                                    <span>Distance:</span>
                                    <span id="distance">-- km</span>
                                </p>
                                <p>
                                    <span>Estimated Duration:</span>
                                    <span id="duration">-- minutes</span>
                                </p>
                                <p>
                                    <span>Estimated Price:</span>
                                    <span id="price">-- UGX</span>
                                </p>
                            </div>
                        </div>

                        <div class="form-group">
                            <label for="specialRequests" class="form-label">Special Requests</label>
                            <textarea id="specialRequests" class="form-control" rows="3" placeholder="Child seats, extra luggage, etc."></textarea>
                        </div>

                        <div class="form-group">
                            <input type="checkbox" id="smsUpdates" checked>
                            <label for="smsUpdates">Receive SMS updates about my booking</label>
                        </div>

                        <button type="button" id="calculateBtn" class="btn btn-block" onclick="calculateRoute()">
                            <span class="btn-text">Calculate Route & Price</span>
                            <span class="btn-spinner" style="display: none;"><i class="fas fa-spinner fa-spin"></i></span>
                        </button>

                        <button type="button" id="bookNowBtn" class="btn btn-block" onclick="openPaymentModal()" disabled>
                            Proceed to Payment
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== Payment Modal ===== -->
    <div class="modal" id="paymentModal">
        <div class="modal-content">
            <span class="close-modal" onclick="closePaymentModal()">×</span>
            <h3 class="modal-title">Complete Your Booking</h3>

            <div class="booking-summary">
                <div class="summary-item">
                    <span>Service:</span>
                    <span id="bookingService">Airport Transfer</span>
                </div>
                <div class="summary-item">
                    <span>From:</span>
                    <span id="bookingFrom">Entebbe Airport</span>
                </div>
                <div class="summary-item">
                    <span>To:</span>
                    <span id="bookingTo">Kampala City Center</span>
                </div>
                <div class="summary-item">
                    <span>Date & Time:</span>
                    <span id="bookingDateTime">15 Jun 2023, 14:30</span>
                </div>
                <div class="summary-item">
                    <span>Passengers:</span>
                    <span id="bookingPassengers">2</span>
                </div>
                <div class="summary-item">
                    <span>Total Price:</span>
                    <span id="bookingPrice">75,000 UGX</span>
                </div>
            </div>

            <div class="payment-options">
                <h4>Select Payment Method</h4>

                <div class="payment-option" onclick="selectPayment('mobile')">
                    <input type="radio" name="paymentMethod" id="mobileMoney" value="mobile" checked>
                    <label for="mobileMoney" class="payment-option-label">
                        <i class="fas fa-mobile-alt"></i> Mobile Money
                    </label>
                </div>

                <div class="payment-form" id="mobileMoneyForm">
                    <div class="form-group">
                        <label for="mobileProvider" class="form-label">Mobile Network</label>
                        <select id="mobileProvider" class="form-control">
                            <option value="mtn">MTN Mobile Money</option>
                            <option value="airtel">Airtel Money</option>
                            <option value="uganda">Uganda Telecom</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="mobileNumber" class="form-label">Phone Number</label>
                        <input type="tel" id="mobileNumber" class="form-control" placeholder="e.g. 0702201096">
                    </div>
                    <button class="btn btn-block" onclick="processMobilePayment()">
                        Pay with Mobile Money
                    </button>
                </div>

                <div class="payment-option" onclick="selectPayment('card')">
                    <input type="radio" name="paymentMethod" id="ugandaCard" value="card">
                    <label for="ugandaCard" class="payment-option-label">
                        <i class="far fa-credit-card"></i> Uganda Card (Visa/Mastercard)
                    </label>
                </div>

                <div class="payment-form" id="cardForm">
                    <div class="form-group">
                        <label for="cardNumber" class="form-label">Card Number</label>
                        <input type="text" id="cardNumber" class="form-control" placeholder="1234 5678 9012 3456">
                    </div>
                    <div class="form-row">
                        <div class="form-group">
                            <label for="expiryDate" class="form-label">Expiry Date</label>
                            <input type="text" id="expiryDate" class="form-control" placeholder="MM/YY">
                        </div>
                        <div class="form-group">
                            <label for="cvv" class="form-label">CVV</label>
                            <input type="text" id="cvv" class="form-control" placeholder="123">
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="cardName" class="form-label">Name on Card</label>
                        <input type="text" id="cardName" class="form-control" placeholder="As shown on card">
                    </div>
                    <button class="btn btn-block" onclick="processCardPayment()">
                        Pay with Card
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- ===== Media Section ===== -->
    <section class="media" id="media">
        <div class="container">
            <h2 class="section-title">Our Journey in Motion</h2>
            <div class="video-player">
                <video id="mainVideo" controls loading="lazy">
                    <source src="https://videos.pexels.com/video-files/855563/855563-hd_1920_1080_30fps.mp4" type="video/mp4">
                    Your browser does not support the video tag.
                </video>
                <div class="video-controls">
                    <button onclick="document.getElementById('mainVideo').play()">Play</button>
                    <button onclick="document.getElementById('mainVideo').pause()">Pause</button>
                    <button onclick="document.getElementById('mainVideo').muted = !document.getElementById('mainVideo').muted">Mute/Unmute</button>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== Robo-Gasion Chatbot ===== -->
    <div class="robo-container">
        <div class="robo-chatbox" id="roboChatbox">
            <div class="robo-header">
                <img src="https://i.imgur.com/JD4s7XW.png" alt="Robo-Gasion">
                <h3>Robo-Gasion Assistant</h3>
                <div class="robo-close" id="roboClose">
                    <i class="fas fa-times"></i>
                </div>
            </div>
            <div class="robo-messages" id="roboMessages">
                <!-- Messages will be added here dynamically -->
            </div>
            <div class="robo-input">
                <input type="text" id="roboInput" placeholder="Ask me about bookings, prices, etc...">
                <button id="roboSend"><i class="fas fa-paper-plane"></i></button>
            </div>
        </div>
        <div class="robo-toggle" id="roboToggle">
            <i class="fas fa-robot"></i>
        </div>
    </div>

    <!-- ===== WhatsApp Float ===== -->
    <a href="https://wa.me/256702201096" class="whatsapp-float" target="_blank" rel="noopener noreferrer">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- ===== Footer ===== -->
    <footer id="contact">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-column">
                    <h3>Our Services</h3>
                    <ul class="footer-links">
                        <li><a href="#services">Airport Transfers</a></li>
                        <li><a href="#services">Wedding Transportation</a></li>
                        <li><a href="#services">Corporate Events</a></li>
                        <li><a href="#services">City Tours</a></li>
                        <li><a href="#services">Special Occasions</a></li>
                        <li><a href="#services">Long Distance</a></li>
                    </ul>
                </div>

                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#booking">Book Now</a></li>
                        <li><a href="#testimonials">Testimonials</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>

                <div class="footer-column">
                    <h3>Contact Us</h3>
                    <ul class="footer-links">
                        <li>
                            <i class="fas fa-phone"></i> +256 702 201096
                        </li>
                        <li>
                            <i class="fas fa-envelope"></i> <a href="mailto:info@gasiontransfers.com">info@gasiontransfers.com</a>
                        </li>
                        <li>
                            <i class="fas fa-map-marker-alt"></i> Kampala, Uganda
                        </li>
                    </ul>

                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="https://wa.me/256702201096"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
            </div>

            <div class="copyright">
                <p>© 2025 Gasion Airport Pick-ups & Drop-offs. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- ===== Leaflet JS and Routing Machine ===== -->
    <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
    <script src="https://unpkg.com/leaflet-routing-machine@3.2.12/dist/leaflet-routing-machine.js"></script>

    <script>
        // ===== Mobile Menu Toggle =====
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navLinks = document.getElementById('navLinks');

        mobileMenuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            mobileMenuBtn.innerHTML = navLinks.classList.contains('active')
                ? '<i class="fas fa-times"></i>'
                : '<i class="fas fa-bars"></i>';
        });

        // ===== Map Functionality =====
        let map;
        let pickupMarker;
        let destinationMarker;
        let routeControl;
        let settingPickup = false;
        let settingDestination = false;

        function initMap() {
            // Initialize map centered on Kampala
            map = L.map('map').setView([0.3136, 32.5811], 12);

            // Add OpenStreetMap tiles
            L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
                attribution: '© <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
            }).addTo(map);

            // Initialize markers
            pickupMarker = L.marker([0.3136, 32.5811], {
                draggable: true,
                icon: L.icon({
                    iconUrl: 'https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.7.1/images/marker-icon.png',
                    iconSize: [25, 41],
                    iconAnchor: [12, 41]
                })
            }).addTo(map).bindPopup('Pickup Location');

            destinationMarker = L.marker([0.3136, 32.5811], {
                draggable: true,
                icon: L.icon({
                    iconUrl: 'https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.7.1/images/marker-icon-2x.png',
                    iconSize: [25, 41],
                    iconAnchor: [12, 41]
                })
            }).addTo(map).bindPopup('Destination');

            // Initialize routing control
            routeControl = L.Routing.control({
                waypoints: [],
                routeWhileDragging: true,
                show: false,
                addWaypoints: false,
                draggableWaypoints: false,
                fitSelectedRoutes: true,
                lineOptions: {
                    styles: [{color: '#FF6B01', opacity: 0.7, weight: 5}]
                }
            }).addTo(map);

            // Event listeners for marker movement
            pickupMarker.on('dragend', updateRoute);
            destinationMarker.on('dragend', updateRoute);

            // Map click handler for setting markers
            map.on('click', async function(e) {
                const latlng = e.latlng;
                if (settingPickup) {
                    pickupMarker.setLatLng(latlng);
                    const reverseGeocode = await reverseGeocode(latlng.lat, latlng.lng);
                    if (reverseGeocode) {
                        document.getElementById('pickupLocation').value = reverseGeocode.display_name;
                    }
                    settingPickup = false;
                    document.getElementById('pickupLocation').focus();
                    updateRoute();
                } else if (settingDestination) {
                    destinationMarker.setLatLng(latlng);
                    const reverseGeocode = await reverseGeocode(latlng.lat, latlng.lng);
                    if (reverseGeocode) {
                        document.getElementById('destination').value = reverseGeocode.display_name;
                    }
                    settingDestination = false;
                    document.getElementById('destination').focus();
                    updateRoute();
                }
            });
        }

        // Geocoding function using Nominatim
        async function geocodeAddress(address) {
            const url = `https://nominatim.openstreetmap.org/search?format=json&q=${encodeURIComponent(address)}&limit=1&countrycodes=ug`;
            try {
                const response = await fetch(url, {
                    headers: { 'User-Agent': 'Gasion Airport Transfers (info@gasiontransfers.com)' }
                });
                const data = await response.json();
                if (data.length > 0) {
                    return {
                        lat: parseFloat(data[0].lat),
                        lon: parseFloat(data[0].lon),
                        display_name: data[0].display_name
                    };
                }
                throw new Error('Address not found');
            } catch (error) {
                console.error('Geocoding error:', error);
                alert('Could not find the address. Please try a more specific location.');
                return null;
            }
        }

        // Reverse geocoding to get address from coordinates
        async function reverseGeocode(lat, lon) {
            const url = `https://nominatim.openstreetmap.org/reverse?format=json&lat=${lat}&lon=${lon}`;
            try {
                const response = await fetch(url, {
                    headers: { 'User-Agent': 'Gasion Airport Transfers (info@gasiontransfers.com)' }
                });
                const data = await response.json();
                return data.display_name ? { display_name: data.display_name } : null;
            } catch (error) {
                console.error('Reverse geocoding error:', error);
                return null;
            }
        }

        // Autocomplete for address inputs
        function addAutocomplete(inputId) {
            const input = document.getElementById(inputId);
            input.addEventListener('input', async function() {
                const query = input.value;
                if (query.length < 3) return;

                const url = `https://nominatim.openstreetmap.org/search?format=json&q=${encodeURIComponent(query)}&limit=5&countrycodes=ug`;
                try {
                    const response = await fetch(url, {
                        headers: { 'User-Agent': 'Gasion Airport Transfers (info@gasiontransfers.com)' }
                    });
                    const data = await response.json();

                    // Remove existing datalist
                    let datalist = document.getElementById(`${inputId}-datalist`);
                    if (datalist) datalist.remove();

                    // Create new datalist
                    datalist = document.createElement('datalist');
                    datalist.id = `${inputId}-datalist`;
                    data.forEach(item => {
                        const option = document.createElement('option');
                        option.value = item.display_name;
                        datalist.appendChild(option);
                    });
                    input.after(datalist);
                    input.setAttribute('list', `${inputId}-datalist`);
                } catch (error) {
                    console.error('Autocomplete error:', error);
                }
            });
        }

        // Set location from quick buttons
        async function setLocation(type, location) {
            const input = type === 'pickup' ? 'pickupLocation' : 'destination';
            document.getElementById(input).value = location;

            const coords = await geocodeAddress(location);
            if (coords) {
                if (type === 'pickup') {
                    pickupMarker.setLatLng([coords.lat, coords.lon]);
                    map.panTo([coords.lat, coords.lon]);
                } else {
                    destinationMarker.setLatLng([coords.lat, coords.lon]);
                    map.panTo([coords.lat, coords.lon]);
                }
                updateRoute();
            }
        }

        // Toggle marker setting on map
        function toggleMarkerSetting(type) {
            settingPickup = type === 'pickup';
            settingDestination = type === 'destination';
            alert(`Click on the map to set the ${type} location`);
        }

        // Calculate route
        async function calculateRoute() {
            const pickup = document.getElementById('pickupLocation').value;
            const destination = document.getElementById('destination').value;
            const phone = document.getElementById('phone').value;

            // Validate phone number
            if (!validatePhone(phone)) {
                document.getElementById('phoneError').style.display = 'block';
                return;
            } else {
                document.getElementById('phoneError').style.display = 'none';
            }

            if (!pickup || !destination) {
                alert('Please enter both pickup and destination locations');
                return;
            }

            // Show loading state
            const btn = document.getElementById('calculateBtn');
            btn.disabled = true;
            btn.querySelector('.btn-text').style.display = 'none';
            btn.querySelector('.btn-spinner').style.display = 'inline-block';

            try {
                const pickupCoords = await geocodeAddress(pickup);
                const destCoords = await geocodeAddress(destination);

                if (pickupCoords && destCoords) {
                    pickupMarker.setLatLng([pickupCoords.lat, pickupCoords.lon]);
                    destinationMarker.setLatLng([destCoords.lat, destCoords.lon]);
                    updateRoute();
                    map.fitBounds([
                        [pickupCoords.lat, pickupCoords.lon],
                        [destCoords.lat, destCoords.lon]
                    ]);
                }
            } catch (error) {
                console.error(error);
            } finally {
                // Hide loading state
                btn.disabled = false;
                btn.querySelector('.btn-text').style.display = 'inline-block';
                btn.querySelector('.btn-spinner').style.display = 'none';
                document.getElementById('bookNowBtn').disabled = false;
            }
        }

        // Update route on map
        function updateRoute() {
            const pickupPos = pickupMarker.getLatLng();
            const destPos = destinationMarker.getLatLng();

            routeControl.setWaypoints([
                L.latLng(pickupPos.lat, pickupPos.lng),
                L.latLng(destPos.lat, destPos.lng)
            ]);

            // Calculate distance (Haversine formula)
            const distance = calculateDistance(
                [pickupPos.lat, pickupPos.lng],
                [destPos.lat, destPos.lng]
            );

            // Update UI
            document.getElementById('distance').textContent = distance.toFixed(1) + ' km';
            document.getElementById('duration').textContent = Math.round(distance * 2.5) + ' minutes';

            // Calculate price (example pricing)
            const baseFee = 15000; // UGX
            const pricePerKm = 3000; // UGX
            const totalPrice = baseFee + (distance * pricePerKm);

            // Format price with commas
            const formattedPrice = Math.round(totalPrice).toLocaleString('en-US');
            document.getElementById('price').textContent = formattedPrice + ' UGX';

            // Show distance info
            document.getElementById('distanceInfo').style.display = 'block';

            // Store booking details
            window.bookingDetails = {
                service: document.getElementById('serviceType').value,
                from: document.getElementById('pickupLocation').value,
                to: document.getElementById('destination').value,
                date: document.getElementById('pickupDate').value,
                time: document.getElementById('pickupTime').value,
                passengers: document.getElementById('passengers').value,
                distance: distance.toFixed(1) + ' km',
                duration: Math.round(distance * 2.5) + ' minutes',
                price: totalPrice,
                formattedPrice: formattedPrice
            };
        }

        // Calculate distance between coordinates (Haversine formula)
        function calculateDistance(coord1, coord2) {
            const R = 6371; // Earth radius in km
            const dLat = (coord2[0] - coord1[0]) * Math.PI / 180;
            const dLon = (coord2[1] - coord1[1]) * Math.PI / 180;
            const a =
                Math.sin(dLat/2) * Math.sin(dLat/2) +
                Math.cos(coord1[0] * Math.PI / 180) * Math.cos(coord2[0] * Math.PI / 180) *
                Math.sin(dLon/2) * Math.sin(dLon/2);
            const c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1-a));
            return R * c;
        }

        // Validate Ugandan phone number
        function validatePhone(phone) {
            return /^(\+?256|0)?[7]\d{8}$/.test(phone);
        }

        // Form validation
        document.getElementById('transportForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const fullName = document.getElementById('fullName').value;
            const phone = document.getElementById('phone').value;
            const email = document.getElementById('email').value;
            const serviceType = document.getElementById('serviceType').value;
            const passengers = document.getElementById('passengers').value;
            const pickupDate = document.getElementById('pickupDate').value;
            const pickupTime = document.getElementById('pickupTime').value;
            const pickupLocation = document.getElementById('pickupLocation').value;
            const destination = document.getElementById('destination').value;

            if (!fullName) {
                alert('Please enter your full name');
                return;
            }
            if (!validatePhone(phone)) {
                document.getElementById('phoneError').style.display = 'block';
                return;
            }
            if (email && !/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)) {
                alert('Please enter a valid email address');
                return;
            }
            if (!serviceType) {
                alert('Please select a service type');
                return;
            }
            if (passengers < 1) {
                alert('Please enter a valid number of passengers');
                return;
            }
            if (!pickupDate || !pickupTime) {
                alert('Please select pickup date and time');
                return;
            }
            if (!pickupLocation || !destination) {
                alert('Please enter both pickup and destination locations');
                return;
            }

            calculateRoute();
        });

        // ===== Payment Modal =====
        function openPaymentModal() {
            if (!window.bookingDetails) {
                alert('Please calculate your route first');
                return;
            }

            // Update booking summary
            document.getElementById('bookingService').textContent =
                document.getElementById('serviceType').options[document.getElementById('serviceType').selectedIndex].text;
            document.getElementById('bookingFrom').textContent = window.bookingDetails.from;
            document.getElementById('bookingTo').textContent = window.bookingDetails.to;
            document.getElementById('bookingDateTime').textContent =
                formatDate(window.bookingDetails.date) + ', ' + window.bookingDetails.time;
            document.getElementById('bookingPassengers').textContent = window.bookingDetails.passengers;
            document.getElementById('bookingPrice').textContent = window.bookingDetails.formattedPrice + ' UGX';

            // Show modal
            document.getElementById('paymentModal').style.display = 'flex';
            document.body.style.overflow = 'hidden';

            // Show mobile money form by default
            selectPayment('mobile');
        }

        function closePaymentModal() {
            document.getElementById('paymentModal').style.display = 'none';
            document.body.style.overflow = 'auto';
        }

        function selectPayment(method) {
            document.getElementById('mobileMoneyForm').style.display = 'none';
            document.getElementById('cardForm').style.display = 'none';

            if (method === 'mobile') {
                document.getElementById('mobileMoneyForm').style.display = 'block';
            } else if (method === 'card') {
                document.getElementById('cardForm').style.display = 'block';
            }
        }

        async function processMobilePayment() {
            const provider = document.getElementById('mobileProvider').value;
            const number = document.getElementById('mobileNumber').value;

            if (!number) {
                alert('Please enter your mobile money number');
                return;
            }

            if (!validatePhone(number)) {
                alert('Please enter a valid Ugandan phone number (e.g. 0702201096 or 256702201096)');
                return;
            }

            // Simulate payment (replace with Flutterwave integration)
            alert(`Payment request sent to ${provider} for ${window.bookingDetails.formattedPrice} UGX. Please complete the payment on your phone.`);

            setTimeout(async () => {
                alert('Payment confirmed! Your booking is complete. We will send you confirmation details shortly.');
                await sendBookingToBackend();
                closePaymentModal();
                resetForm();
            }, 2000);

            /* Uncomment for Flutterwave integration
            const email = document.getElementById('email').value || 'no-email@gasiontransfers.com';
            try {
                const response = await FlutterwaveCheckout({
                    public_key: 'YOUR_FLUTTERWAVE_PUBLIC_KEY',
                    tx_ref: `GASON-${Date.now()}`,
                    amount: window.bookingDetails.price,
                    currency: 'UGX',
                    payment_options: 'mobilemoneyuganda',
                    customer: {
                        email: email,
                        phone_number: number,
                        name: document.getElementById('fullName').value
                    },
                    customizations: {
                        title: 'Gasion Airport Transfers',
                        description: `Payment for ${window.bookingDetails.service} from ${window.bookingDetails.from} to ${window.bookingDetails.to}`,
                        logo: 'https://your-logo-url.com/logo.png'
                    }
                });

                if (response.status === 'successful') {
                    alert('Payment successful! Your booking is complete.');
                    await sendBookingToBackend();
                    closePaymentModal();
                    resetForm();
                }
            } catch (error) {
                console.error('Payment error:', error);
                alert('Payment failed. Please try again.');
            }
            */
        }

        async function processCardPayment() {
            const cardNumber = document.getElementById('cardNumber').value;
            const expiry = document.getElementById('expiryDate').value;
            const cvv = document.getElementById('cvv').value;
            const name = document.getElementById('cardName').value;

            if (!cardNumber || !expiry || !cvv || !name) {
                alert('Please fill in all card details');
                return;
            }

            if (!/^\d{16}$/.test(cardNumber.replace(/\s/g, ''))) {
                alert('Please enter a valid 16-digit card number');
                return;
            }

            if (!/^\d{3,4}$/.test(cvv)) {
                alert('Please enter a valid CVV');
                return;
            }

            // Simulate payment (replace with Flutterwave integration)
            alert(`Processing card payment for ${window.bookingDetails.formattedPrice} UGX...`);

            setTimeout(async () => {
                alert('Payment successful! Your booking is complete. We will send you confirmation details shortly.');
                await sendBookingToBackend();
                closePaymentModal();
                resetForm();
            }, 2000);

            /* Uncomment for Flutterwave integration
            const email = document.getElementById('email').value || 'no-email@gasiontransfers.com';
            try {
                const response = await FlutterwaveCheckout({
                    public_key: 'YOUR_FLUTTERWAVE_PUBLIC_KEY',
                    tx_ref: `GASON-${Date.now()}`,
                    amount: window.bookingDetails.price,
                    currency: 'UGX',
                    payment_options: 'card',
                    customer: {
                        email: email,
                        phone_number: document.getElementById('phone').value,
                        name: name
                    },
                    customizations: {
                        title: 'Gasion Airport Transfers',
                        description: `Payment for ${window.bookingDetails.service} from ${window.bookingDetails.from} to ${window.bookingDetails.to}`,
                        logo: 'https://your-logo-url.com/logo.png'
                    }
                });

                if (response.status === 'successful') {
                    alert('Payment successful! Your booking is complete.');
                    await sendBookingToBackend();
                    closePaymentModal();
                    resetForm();
                }
            } catch (error) {
                console.error('Payment error:', error);
                alert('Payment failed. Please try again.');
            }
            */
        }

        // Send booking to backend
        async function sendBookingToBackend() {
            try {
                const response = await fetch('/api/bookings', {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({
                        fullName: document.getElementById('fullName').value,
                        phone: document.getElementById('phone').value,
                        email: document.getElementById('email').value,
                        serviceType: document.getElementById('serviceType').value,
                        passengers: document.getElementById('passengers').value,
                        pickupDate: document.getElementById('pickupDate').value,
                        pickupTime: document.getElementById('pickupTime').value,
                        pickupLocation: document.getElementById('pickupLocation').value,
                        destination: document.getElementById('destination').value,
                        specialRequests: document.getElementById('specialRequests').value,
                        bookingDetails: window.bookingDetails
                    })
                });
                if (!response.ok) throw new Error('Failed to save booking');
            } catch (error) {
                console.error('Backend error:', error);
                alert('Booking saved locally, but there was an issue syncing with our servers. We will contact you soon.');
            }
        }

        // Format date for display
        function formatDate(dateString) {
            if (!dateString) return '--';
            const options = { day: 'numeric', month: 'short', year: 'numeric' };
            return new Date(dateString).toLocaleDateString('en-US', options);
        }

        // Reset form after successful booking
        function resetForm() {
            document.getElementById('transportForm').reset();
            document.getElementById('distanceInfo').style.display = 'none';
            document.getElementById('bookNowBtn').disabled = true;

            // Reset map
            pickupMarker.setLatLng([0.3136, 32.5811]);
            destinationMarker.setLatLng([0.3136, 32.5811]);
            map.setView([0.3136, 32.5811], 12);
            routeControl.setWaypoints([]);
        }

        // Close modal when clicking outside
        window.addEventListener('click', function(event) {
            if (event.target === document.getElementById('paymentModal')) {
                closePaymentModal();
            }
        });

        // Robo-Gasion Chatbot Functionality
        const roboToggle = document.getElementById('roboToggle');
        const roboChatbox = document.getElementById('roboChatbox');
        const roboClose = document.getElementById('roboClose');
        const roboMessages = document.getElementById('roboMessages');
        const roboInput = document.getElementById('roboInput');
        const roboSend = document.getElementById('roboSend');

        // Initial bot message
        const initialMessages = [
            {
                text: "Hello! I'm Robo-Gasion, your virtual assistant. How can I help you today?",
                sender: 'bot',
                quickReplies: [
                    "Book airport transfer",
                    "Get price estimate",
                    "Check booking status",
                    "Talk to human agent"
                ]
            }
        ];

        // Luganda responses
        const lugandaMessages = {
            greeting: "Nkulamusizza! Nze Robo-Gasion. Nsobola okukuyamba ki?",
            options: [
                "Okutambuza ku ddoboozi",
                "Okutegeeza ssente",
                "Okukebejja booking yo",
                "Kuba n'omuntu"
            ]
        };

        let currentLanguage = 'english';

        // Toggle chatbox
        roboToggle.addEventListener('click', () => {
            roboChatbox.classList.toggle('active');
            if (roboChatbox.classList.contains('active') && roboMessages.children.length === 0) {
                displayMessages(initialMessages);
            }
        });

        roboClose.addEventListener('click', () => {
            roboChatbox.classList.remove('active');
        });

        // Send message function
        function sendMessage() {
            const messageText = roboInput.value.trim();
            if (messageText === '') return;

            addMessage(messageText, 'user');
            roboInput.value = '';

            // Simulate bot response
            setTimeout(() => {
                handleUserInput(messageText.toLowerCase());
            }, 500);
        }

        // Handle user# gasionairportpickup
