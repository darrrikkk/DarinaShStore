<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DarinaShStore - Все для ваших питомцев</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Основные стили */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary-color: rgb(153, 181, 109);
            --primary-dark: rgb(133, 161, 89);
            --primary-light: rgb(173, 201, 129);
            --accent-color: #FF7B54;
            --accent-light: #FF9B7B;
            --secondary-color: #6A8CAF;
            --secondary-light: #8CA9C5;
            --text-color: #333;
            --light-bg: #f9f9f9;
            --white: #ffffff;
            --gray: #777;
            --light-gray: #e0e0e0;
            --shadow: 0 5px 15px rgba(0,0,0,0.1);
            --transition: all 0.3s ease;
        }
        
        body {
            background-color: var(--light-bg);
            color: var(--text-color);
            line-height: 1.6;
            padding-top: 80px; /* Отступ для фиксированного хедера */
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Шапка сайта */
        header {
            background-color: var(--white);
            box-shadow: var(--shadow);
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            transition: var(--transition);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
            flex-shrink: 0;
        }
        
        .logo i {
            font-size: 2rem;
            color: var(--primary-color);
            margin-right: 10px;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            color: var(--primary-color);
            font-weight: 700;
        }
        
        .search-bar {
            flex-grow: 1;
            max-width: 500px;
            margin: 0 20px;
            display: flex;
        }
        
        .search-bar input {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid var(--primary-color);
            border-radius: 30px 0 0 30px;
            font-size: 1rem;
            outline: none;
            transition: var(--transition);
        }
        
        .search-bar input:focus {
            border-color: var(--accent-color);
        }
        
        .search-bar button {
            background-color: var(--primary-color);
            color: white;
            border: none;
            border-radius: 0 30px 30px 0;
            padding: 0 20px;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .search-bar button:hover {
            background-color: var(--primary-dark);
        }
        
        .user-actions {
            display: flex;
            gap: 15px;
        }
        
        .user-actions a {
            color: var(--primary-color);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 5px;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }
        
        .user-actions a:hover {
            color: var(--accent-color);
        }
        
        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background-color: var(--accent-color);
            color: white;
            border-radius: 50%;
            width: 18px;
            height: 18px;
            font-size: 0.7rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        /* Навигация */
        nav {
            background-color: var(--primary-color);
            transition: var(--transition);
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .nav-menu {
            display: flex;
            list-style: none;
            flex-wrap: wrap;
        }
        
        .nav-menu li a {
            color: white;
            text-decoration: none;
            padding: 12px 15px;
            border-radius: 4px;
            transition: var(--transition);
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 5px;
            white-space: nowrap;
        }
        
        .nav-menu li a:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }
        
        .nav-menu li a.active {
            background-color: var(--accent-color);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Главный баннер */
        .hero {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-bottom: 40px;
            border-radius: 0 0 30px 30px;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000" opacity="0.1"><path fill="white" d="M430 150c0 50-40 90-90 90s-90-40-90-90 40-90 90-90 90 40 90 90zm470 190c0 50-40 90-90 90s-90-40-90-90 40-90 90-90 90 40 90 90zm-940 50c0 50-40 90-90 90s-90-40-90-90 40-90 90-90 90 40 90 90zm390 430c0 50-40 90-90 90s-90-40-90-90 40-90 90-90 90 40 90 90zm280-560c0 50-40 90-90 90s-90-40-90-90 40-90 90-90 90 40 90 90zm360 180c0 50-40 90-90 90s-90-40-90-90 40-90 90-90 90 40 90 90z"/></svg>');
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 0 20px;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
            font-weight: 800;
        }
        
        .slogan {
            font-size: 2rem;
            font-weight: bold;
            color: #fff;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
            margin-bottom: 20px;
            position: relative;
            display: inline-block;
        }
        
        .slogan::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background-color: var(--accent-color);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .cta-button {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 15px 35px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            margin-top: 20px;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            border: 2px solid var(--accent-color);
        }
        
        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
            background-color: transparent;
            color: var(--accent-color);
        }
        
        /* Основной контент */
        main {
            padding: 20px 0 40px;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: var(--primary-color);
            position: relative;
            font-size: 2.2rem;
            font-weight: 700;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--primary-color), var(--accent-color));
            margin: 15px auto;
            border-radius: 2px;
        }
        
        /* Категории товаров */
        .categories {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 50px;
        }
        
        .category-card {
            background: var(--white);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            text-align: center;
            cursor: pointer;
            position: relative;
            border: 2px solid transparent;
        }
        
        .category-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 25px rgba(0,0,0,0.15);
            border-color: var(--primary-color);
        }
        
        .category-icon {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            padding: 25px;
            font-size: 2.5rem;
            color: white;
            transition: var(--transition);
        }
        
        .category-card:hover .category-icon {
            background: linear-gradient(135deg, var(--accent-color), var(--accent-light));
        }
        
        .category-card h3 {
            padding: 20px 15px;
            color: var(--primary-color);
            font-size: 1.3rem;
            transition: var(--transition);
        }
        
        .category-card:hover h3 {
            color: var(--accent-color);
        }
        
        /* Популярные товары */
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 50px;
        }
        
        .product-card {
            background: var(--white);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.15);
        }
        
        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--accent-color);
            color: white;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
            z-index: 2;
        }
        
        .product-image {
            height: 200px;
            background: linear-gradient(135deg, var(--primary-light), var(--secondary-light));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
            position: relative;
            overflow: hidden;
        }
        
        .product-image::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" opacity="0.1"><circle cx="50" cy="50" r="40" fill="white"/></svg>');
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-info h3 {
            margin-bottom: 10px;
            color: var(--primary-color);
            font-size: 1.2rem;
        }
        
        .product-info p {
            color: var(--gray);
            font-size: 0.9rem;
            margin-bottom: 15px;
        }
        
        .product-price {
            font-weight: bold;
            color: var(--accent-color);
            font-size: 1.3rem;
            margin: 10px 0;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .old-price {
            text-decoration: line-through;
            color: var(--gray);
            font-size: 1rem;
        }
        
        .add-to-cart {
            background: linear-gradient(to right, var(--primary-color), var(--primary-dark));
            color: white;
            border: none;
            padding: 12px 15px;
            border-radius: 8px;
            width: 100%;
            cursor: pointer;
            font-weight: bold;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        
        .add-to-cart:hover {
            background: linear-gradient(to right, var(--accent-color), var(--accent-light));
            transform: translateY(-2px);
        }
        
        /* Контактная информация */
        .contact-info {
            background: linear-gradient(135deg, var(--white) 0%, var(--light-bg) 100%);
            border-radius: 15px;
            padding: 30px;
            box-shadow: var(--shadow);
            margin-bottom: 40px;
            border: 1px solid var(--light-gray);
        }
        
        .contact-details {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 15px;
        }
        
        .contact-item i {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            flex-shrink: 0;
        }
        
        /* Поддержка */
        .support {
            background: linear-gradient(135deg, var(--white) 0%, var(--light-bg) 100%);
            border-radius: 15px;
            padding: 30px;
            box-shadow: var(--shadow);
            border: 1px solid var(--light-gray);
        }
        
        .support-form {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--primary-color);
        }
        
        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid var(--light-gray);
            border-radius: 8px;
            font-size: 1rem;
            transition: var(--transition);
        }
        
        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            border-color: var(--primary-color);
            outline: none;
            box-shadow: 0 0 0 3px rgba(153, 181, 109, 0.2);
        }
        
        .submit-btn {
            background: linear-gradient(to right, var(--primary-color), var(--primary-dark));
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            margin: 0 auto;
        }
        
        .submit-btn:hover {
            background: linear-gradient(to right, var(--accent-color), var(--accent-light));
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        /* Футер */
        footer {
            background: linear-gradient(135deg, var(--primary-dark) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-column h3 {
            margin-bottom: 20px;
            font-size: 1.3rem;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 2px;
            background-color: var(--accent-color);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #e0e0e0;
            text-decoration: none;
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .footer-column ul li a:hover {
            color: white;
            transform: translateX(5px);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: var(--transition);
        }
        
        .social-links a:hover {
            background-color: var(--accent-color);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            color: #e0e0e0;
        }
        
        /* Адаптивность */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 2.5rem;
            }
            
            .slogan {
                font-size: 1.8rem;
            }
        }
        
        @media (max-width: 768px) {
            body {
                padding-top: 70px;
            }
            
            .header-container {
                flex-wrap: wrap;
            }
            
            .logo h1 {
                font-size: 1.5rem;
            }
            
            .search-bar {
                order: 3;
                width: 100%;
                max-width: 100%;
                margin: 15px 0 0;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .nav-menu {
                display: none;
                flex-direction: column;
                width: 100%;
                position: absolute;
                top: 100%;
                left: 0;
                background-color: var(--primary-color);
                box-shadow: var(--shadow);
                z-index: 100;
            }
            
            .nav-menu.active {
                display: flex;
            }
            
            .nav-menu li {
                width: 100%;
            }
            
            .nav-menu li a {
                padding: 15px 20px;
                border-radius: 0;
                border-bottom: 1px solid rgba(255,255,255,0.1);
            }
            
            .hero {
                height: 400px;
                border-radius: 0 0 20px 20px;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .slogan {
                font-size: 1.5rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
        }
        
        @media (max-width: 576px) {
            .hero {
                height: 350px;
            }
            
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .slogan {
                font-size: 1.3rem;
            }
            
            .categories, .products {
                grid-template-columns: 1fr;
            }
            
            .user-actions span {
                display: none;
            }
            
            .user-actions a {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Шапка сайта -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-paw"></i>
                <h1>DarinaShStore</h1>
            </div>
            <div class="search-bar">
                <input type="text" placeholder="Поиск товаров...">
                <button><i class="fas fa-search"></i></button>
            </div>
            <div class="user-actions">
                <a href="#"><i class="fas fa-user"></i> <span>Войти</span></a>
                <a href="#"><i class="fas fa-shopping-cart"></i> <span>Корзина</span> <span class="cart-count">3</span></a>
            </div>
        </div>
        <nav>
            <div class="container nav-container">
                <button class="mobile-menu-btn">
                    <i class="fas fa-bars"></i>
                </button>
                <ul class="nav-menu">
                    <li><a href="#" class="active"><i class="fas fa-home"></i> Главная</a></li>
                    <li><a href="#"><i class="fas fa-dog"></i> Для собак</a></li>
                    <li><a href="#"><i class="fas fa-cat"></i> Для кошек</a></li>
                    <li><a href="#"><i class="fas fa-kiwi-bird"></i> Для птиц</a></li>
                    <li><a href="#"><i class="fas fa-fish"></i> Для рыбок</a></li>
                    <li><a href="#"><i class="fas fa-paw"></i> Для грызунов</a></li>
                    <li><a href="#"><i class="fas fa-map-marker-alt"></i> Магазины</a></li>
                    <li><a href="#"><i class="fas fa-headset"></i> Поддержка</a></li>
                </ul>
            </div>
        </nav>
    </header>

    <!-- Главный баннер -->
    <section class="hero">
        <div class="hero-content">
            <h2>DarinaShStore</h2>
            <div class="slogan">Пушистик будет рад!</div>
            <p>Всё для здоровья и радости ваших питомцев. Широкий ассортимент товаров по доступным ценам.</p>
            <a href="#" class="cta-button">Перейти к покупкам <i class="fas fa-arrow-right"></i></a>
        </div>
    </section>

    <!-- Основной контент -->
    <main class="container">
        <!-- Категории товаров -->
        <section>
            <h2 class="section-title">Категории товаров</h2>
            <div class="categories">
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-dog"></i>
                    </div>
                    <h3>Для собак</h3>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-cat"></i>
                    </div>
                    <h3>Для кошек</h3>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-fish"></i>
                    </div>
                    <h3>Для рыбок</h3>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-kiwi-bird"></i>
                    </div>
                    <h3>Для птиц</h3>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-paw"></i>
                    </div>
                    <h3>Для грызунов</h3>
                </div>
                <div class="category-card">
                    <div class="category-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Ветеринария</h3>
                </div>
            </div>
        </section>

        <!-- Популярные товары -->
        <section>
            <h2 class="section-title">Популярные товары</h2>
            <div class="products">
                <div class="product-card">
                    <div class="product-badge">Хит</div>
                    <div class="product-image">
                        <i class="fas fa-bone"></i>
                    </div>
                    <div class="product-info">
                        <h3>Сухой корм для собак</h3>
                        <p>Полнорационный корм премиум-класса для активных собак</p>
                        <div class="product-price">
                            <span>1 299 ₽</span>
                            <span class="old-price">1 599 ₽</span>
                        </div>
                        <button class="add-to-cart"><i class="fas fa-shopping-cart"></i> В корзину</button>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-badge">Акция</div>
                    <div class="product-image">
                        <i class="fas fa-fish"></i>
                    </div>
                    <div class="product-info">
                        <h3>Корм для кошек</h3>
                        <p>Влажный корм с лососем и тунцом для привередливых кошек</p>
                        <div class="product-price">
                            <span>849 ₽</span>
                        </div>
                        <button class="add-to-cart"><i class="fas fa-shopping-cart"></i> В корзину</button>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-image">
                        <i class="fas fa-home"></i>
                    </div>
                    <div class="product-info">
                        <h3>Домик для кошки</h3>
                        <p>Уютный домик с когтеточкой и игровыми элементами</p>
                        <div class="product-price">
                            <span>3 499 ₽</span>
                        </div>
                        <button class="add-to-cart"><i class="fas fa-shopping-cart"></i> В корзину</button>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-badge">Новинка</div>
                    <div class="product-image">
                        <i class="fas fa-tshirt"></i>
                    </div>
                    <div class="product-info">
                        <h3>Одежда для собак</h3>
                        <p>Теплый комбинезон для прогулок в холодную погоду</p>
                        <div class="product-price">
                            <span>1 899 ₽</span>
                        </div>
                        <button class="add-to-cart"><i class="fas fa-shopping-cart"></i> В корзину</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Контактная информация -->
        <section>
            <h2 class="section-title">Наши магазины</h2>
            <div class="contact-info">
                <p>Посетите один из наших магазинов, где наши консультанты помогут подобрать всё необходимое для вашего питомца.</p>
                <div class="contact-details">
                    <div>
                        <h3>Основной магазин</h3>
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <div>ул. Пушкинская, 15</div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-clock"></i>
                            <div>Ежедневно с 9:00 до 21:00</div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <div>+7 (495) 123-45-67</div>
                        </div>
                    </div>
                    <div>
                        <h3>Филиал на западе</h3>
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <div>пр. Мира, 42, ТЦ "ЗооМир"</div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-clock"></i>
                            <div>Ежедневно с 10:00 до 22:00</div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <div>+7 (495) 765-43-21</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Поддержка -->
        <section>
            <h2 class="section-title">Обращение в техподдержку</h2>
            <div class="support">
                <div class="support-form">
                    <div class="form-group">
                        <label for="name">Ваше имя</label>
                        <input type="text" id="name" placeholder="Введите ваше имя">
                    </div>
                    <div class="form-group">
                        <label for="email">Электронная почта</label>
                        <input type="email" id="email" placeholder="Введите ваш email">
                    </div>
                    <div class="form-group">
                        <label for="subject">Тема обращения</label>
                        <select id="subject">
                            <option value="">Выберите тему</option>
                            <option value="problem">Проблема с заказом</option>
                            <option value="question">Вопрос о товаре</option>
                            <option value="return">Возврат товара</option>
                            <option value="other">Другое</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message">Сообщение</label>
                        <textarea id="message" rows="5" placeholder="Опишите вашу проблему или вопрос"></textarea>
                    </div>
                    <button type="submit" class="submit-btn"><i class="fas fa-paper-plane"></i> Отправить сообщение</button>
                </div>
            </div>
        </section>
    </main>

    <!-- Футер -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>DarinaShStore</h3>
                    <p>Все для ваших питомцев с любовью и заботой. Мы работаем, чтобы ваш пушистик был рад!</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-vk"></i></a>
                        <a href="#"><i class="fab fa-telegram"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Категории</h3>
                    <ul>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Для собак</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Для кошек</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Для птиц</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Для грызунов</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Для рыбок</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Ветеринария</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Помощь</h3>
                    <ul>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Доставка и оплата</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Возврат товара</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Частые вопросы</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Отзывы</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Контакты</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Контакты</h3>
                    <ul>
                        <li><a href="#"><i class="fas fa-phone"></i> +7 (495) 123-45-67</a></li>
                        <li><a href="#"><i class="fas fa-envelope"></i> info@darinashstore.ru</a></li>
                        <li><a href="#"><i class="fas fa-map-marker-alt"></i> г. Москва, ул. Пушкинская, 15</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                &copy; 2023 DarinaShStore. Все права защищены.
            </div>
        </div>
    </footer>

    <script>
        // Мобильное меню
        document.querySelector('.mobile-menu-btn').addEventListener('click', function() {
            document.querySelector('.nav-menu').classList.toggle('active');
        });

        // Закрытие меню при клике вне его
        document.addEventListener('click', function(event) {
            const navMenu = document.querySelector('.nav-menu');
            const mobileBtn = document.querySelector('.mobile-menu-btn');
            
            if (!navMenu.contains(event.target) && !mobileBtn.contains(event.target)) {
                navMenu.classList.remove('active');
            }
        });

        // Простой скрипт для имитации добавления в корзину
        document.querySelectorAll('.add-to-cart').forEach(button => {
            button.addEventListener('click', function() {
                const productName = this.parentElement.querySelector('h3').textContent;
                const cartCount = document.querySelector('.cart-count');
                let count = parseInt(cartCount.textContent);
                count++;
                cartCount.textContent = count;
                
                // Анимация кнопки
                this.innerHTML = '<i class="fas fa-check"></i> Добавлено';
                this.style.background = 'linear-gradient(to right, var(--accent-color), var(--accent-light))';
                
                setTimeout(() => {
                    this.innerHTML = '<i class="fas fa-shopping-cart"></i> В корзину';
                    this.style.background = 'linear-gradient(to right, var(--primary-color), var(--primary-dark))';
                }, 2000);
                
                // Уведомление
                alert(`Товар "${productName}" добавлен в корзину!`);
            });
        });
        
        // Обработка формы поддержки
        document.querySelector('.submit-btn').addEventListener('click', function(e) {
            e.preventDefault();
            const originalText = this.innerHTML;
            this.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Отправка...';
            this.disabled = true;
            
            setTimeout(() => {
                this.innerHTML = '<i class="fas fa-check"></i> Отправлено!';
                setTimeout(() => {
                    this.innerHTML = originalText;
                    this.disabled = false;
                    document.querySelector('.support-form').reset();
                    alert('Ваше обращение отправлено! Мы свяжемся с вами в ближайшее время.');
                }, 1500);
            }, 2000);
        });

        // Плавная прокрутка для якорных ссылок
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 100,
                        behavior: 'smooth'
                    });
                    
                    // Закрытие мобильного меню после клика
                    document.querySelector('.nav-menu').classList.remove('active');
                }
            });
        });
    </script>
</body>
</html>
