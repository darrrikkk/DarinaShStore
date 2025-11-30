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
            --text-color: #333;
            --light-bg: #f9f9f9;
            --white: #ffffff;
            --gray: #777;
        }
        
        body {
            background-color: var(--light-bg);
            color: var(--text-color);
            line-height: 1.6;
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
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
            flex-wrap: wrap;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo i {
            font-size: 2rem;
            color: var(--primary-color);
            margin-right: 10px;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            color: var(--primary-color);
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
        }
        
        .search-bar button {
            background-color: var(--primary-color);
            color: white;
            border: none;
            border-radius: 0 30px 30px 0;
            padding: 0 20px;
            cursor: pointer;
            transition: background-color 0.3s;
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
            transition: color 0.3s;
        }
        
        .user-actions a:hover {
            color: var(--primary-dark);
        }
        
        /* Навигация */
        nav {
            background-color: var(--primary-color);
            padding: 12px 0;
        }
        
        .nav-menu {
            display: flex;
            list-style: none;
            justify-content: space-around;
            flex-wrap: wrap;
        }
        
        .nav-menu li a {
            color: white;
            text-decoration: none;
            padding: 8px 15px;
            border-radius: 4px;
            transition: background-color 0.3s;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .nav-menu li a:hover {
            background-color: var(--primary-dark);
        }
        
        /* Главный баннер */
        .hero {
            background: linear-gradient(rgba(153, 181, 109, 0.8), rgba(153, 181, 109, 0.9)), url('https://images.unsplash.com/photo-1450778869180-41d0601e046e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-bottom: 40px;
        }
        
        .hero-content h2 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }
        
        .slogan {
            font-size: 1.8rem;
            font-weight: bold;
            color: #fff;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
            margin-bottom: 20px;
        }
        
        .cta-button {
            display: inline-block;
            background-color: white;
            color: var(--primary-color);
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            margin-top: 20px;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.3);
        }
        
        /* Основной контент */
        main {
            padding: 20px 0 40px;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 30px;
            color: var(--primary-color);
            position: relative;
            font-size: 2rem;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--primary-color);
            margin: 10px auto;
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
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            text-align: center;
            cursor: pointer;
        }
        
        .category-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 25px rgba(0,0,0,0.15);
        }
        
        .category-icon {
            background-color: var(--primary-light);
            padding: 25px;
            font-size: 2.5rem;
            color: white;
        }
        
        .category-card h3 {
            padding: 20px 15px;
            color: var(--primary-color);
            font-size: 1.3rem;
        }
        
        /* Популярные товары */
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 25px;
            margin-bottom: 50px;
        }
        
        .product-card {
            background: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: scale(1.03);
        }
        
        .product-image {
            height: 180px;
            background-color: var(--primary-light);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }
        
        .product-info {
            padding: 15px;
        }
        
        .product-info h3 {
            margin-bottom: 10px;
            color: var(--primary-color);
        }
        
        .product-price {
            font-weight: bold;
            color: var(--primary-dark);
            font-size: 1.2rem;
            margin: 10px 0;
        }
        
        .add-to-cart {
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            width: 100%;
            cursor: pointer;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .add-to-cart:hover {
            background-color: var(--primary-dark);
        }
        
        /* Контактная информация */
        .contact-info {
            background-color: var(--white);
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            margin-bottom: 40px;
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
            background-color: var(--primary-light);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
        }
        
        /* Поддержка */
        .support {
            background-color: var(--white);
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
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
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            border-color: var(--primary-color);
            outline: none;
        }
        
        .submit-btn {
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .submit-btn:hover {
            background-color: var(--primary-dark);
        }
        
        /* Футер */
        footer {
            background-color: var(--primary-dark);
            color: white;
            padding: 40px 0 20px;
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
            background-color: white;
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
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: white;
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
            width: 36px;
            height: 36px;
            background-color: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .social-links a:hover {
            background-color: rgba(255,255,255,0.2);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            color: #e0e0e0;
        }
        
        /* Адаптивность */
        @media (max-width: 768px) {
            .header-top {
                flex-direction: column;
                gap: 15px;
            }
            
            .search-bar {
                width: 100%;
                max-width: 100%;
                margin: 10px 0;
            }
            
            .nav-menu {
                flex-direction: column;
                gap: 10px;
            }
            
            .hero {
                height: 300px;
            }
            
            .hero-content h2 {
                font-size: 2rem;
            }
            
            .slogan {
                font-size: 1.4rem;
            }
        }
    </style>
</head>
<body>
    <!-- Шапка сайта -->
    <header>
        <div class="container">
            <div class="header-top">
                <div class="logo">
                    <i class="fas fa-paw"></i>
                    <h1>DarinaShStore</h1>
                </div>
                <div class="search-bar">
                    <input type="text" placeholder="Поиск товаров...">
                    <button><i class="fas fa-search"></i></button>
                </div>
                <div class="user-actions">
                    <a href="#"><i class="fas fa-user"></i> Войти</a>
                    <a href="#"><i class="fas fa-shopping-cart"></i> Корзина</a>
                </div>
            </div>
        </div>
        <nav>
            <div class="container">
                <ul class="nav-menu">
                    <li><a href="#"><i class="fas fa-home"></i> Главная</a></li>
                    <li><a href="#"><i class="fas fa-dog"></i> Для собак</a></li>
                    <li><a href="#"><i class="fas fa-cat"></i> Для кошек</a></li>
                    <li><a href="#"><i class="fas fa-fish"></i> Для грызунов</a></li>
                    <li><a href="#"><i class="fas fa-shopping-basket"></i> Акции</a></li>
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
            <p>Всё для здоровья и радости ваших питомцев</p>
            <a href="#" class="cta-button">Перейти к покупкам</a>
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
                    <div class="product-image">
                        <i class="fas fa-bone"></i>
                    </div>
                    <div class="product-info">
                        <h3>Сухой корм для собак</h3>
                        <p>Полнорационный корм премиум-класса</p>
                        <div class="product-price">1 299 ₽</div>
                        <button class="add-to-cart">В корзину</button>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-image">
                        <i class="fas fa-fish"></i>
                    </div>
                    <div class="product-info">
                        <h3>Корм для кошек</h3>
                        <p>Влажный корм с лососем и тунцом</p>
                        <div class="product-price">849 ₽</div>
                        <button class="add-to-cart">В корзину</button>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-image">
                        <i class="fas fa-home"></i>
                    </div>
                    <div class="product-info">
                        <h3>Домик для кошки</h3>
                        <p>Уютный домик с когтеточкой</p>
                        <div class="product-price">3 499 ₽</div>
                        <button class="add-to-cart">В корзину</button>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-image">
                        <i class="fas fa-tshirt"></i>
                    </div>
                    <div class="product-info">
                        <h3>Одежда для собак</h3>
                        <p>Теплый комбинезон для прогулок</p>
                        <div class="product-price">1 899 ₽</div>
                        <button class="add-to-cart">В корзину</button>
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
                        <input type="text" id="subject" placeholder="Тема вашего обращения">
                    </div>
                    <div class="form-group">
                        <label for="message">Сообщение</label>
                        <textarea id="message" rows="5" placeholder="Опишите вашу проблему или вопрос"></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Отправить сообщение</button>
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
                        <li><a href="#">Для собак</a></li>
                        <li><a href="#">Для кошек</a></li>
                        <li><a href="#">Для птиц</a></li>
                        <li><a href="#">Для грызунов</a></li>
                        <li><a href="#">Для рыбок</a></li>
                        <li><a href="#">Ветеринария</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Помощь</h3>
                    <ul>
                        <li><a href="#">Доставка и оплата</a></li>
                        <li><a href="#">Возврат товара</a></li>
                        <li><a href="#">Частые вопросы</a></li>
                        <li><a href="#">Отзывы</a></li>
                        <li><a href="#">Контакты</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Контакты</h3>
                    <ul>
                        <li><i class="fas fa-phone"></i> +7 (495) 123-45-67</li>
                        <li><i class="fas fa-envelope"></i> info@darinashstore.ru</li>
                        <li><i class="fas fa-map-marker-alt"></i> г. Москва, ул. Пушкинская, 15</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                &copy; 2023 DarinaShStore. Все права защищены.
            </div>
        </div>
    </footer>

    <script>
        // Простой скрипт для имитации добавления в корзину
        document.querySelectorAll('.add-to-cart').forEach(button => {
            button.addEventListener('click', function() {
                const productName = this.parentElement.querySelector('h3').textContent;
                alert(`Товар "${productName}" добавлен в корзину!`);
            });
        });
        
        // Обработка формы поддержки
        document.querySelector('.submit-btn').addEventListener('click', function(e) {
            e.preventDefault();
            alert('Ваше обращение отправлено! Мы свяжемся с вами в ближайшее время.');
            document.querySelector('.support-form').reset();
        });
    </script>
</body>
</html>
