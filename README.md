<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Зефирный Сад — Букеты из зефира</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', sans-serif;
            background-color: #fdf8f5;
            color: #3d2c2a;
            line-height: 1.6;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        .header {
            padding: 25px 0;
            border-bottom: 2px solid #fce4e0;
        }
        .header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }
        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 28px;
            font-weight: 700;
            color: #b34a6b;
            letter-spacing: 1px;
        }
        .logo span {
            color: #e8a0b4;
        }
        .phone {
            background: #b34a6b;
            color: #fff;
            padding: 10px 25px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 16px;
            transition: 0.3s;
            box-shadow: 0 4px 10px rgba(179, 74, 107, 0.3);
        }
        .phone:hover {
            background: #9c3d5a;
            transform: scale(1.03);
        }
        .hero {
            padding: 60px 0 80px;
        }
        .hero .container {
            display: flex;
            align-items: center;
            gap: 50px;
            flex-wrap: wrap;
        }
        .hero-text {
            flex: 1 1 45%;
        }
        .hero-text h1 {
            font-family: 'Playfair Display', serif;
            font-size: 52px;
            line-height: 1.2;
            color: #2d1f1c;
            margin-bottom: 20px;
        }
        .hero-text h1 span {
            color: #b34a6b;
            background: linear-gradient(145deg, #f8d5da, #fce4e0);
            padding: 0 12px;
            display: inline-block;
            border-radius: 20px 0 20px 0;
        }
        .hero-text p {
            font-size: 20px;
            color: #5f4a46;
            margin-bottom: 35px;
            max-width: 500px;
        }
        .btn-primary {
            display: inline-block;
            background: #b34a6b;
            color: #fff;
            padding: 16px 45px;
            border-radius: 60px;
            text-decoration: none;
            font-weight: 600;
            font-size: 18px;
            box-shadow: 0 8px 25px rgba(179, 74, 107, 0.35);
            transition: 0.3s;
            border: none;
            cursor: pointer;
        }
        .btn-primary:hover {
            background: #8f3a55;
            transform: translateY(-3px);
        }
        .hero-image {
            flex: 1 1 45%;
            background: linear-gradient(135deg, #fce4e0, #f8d5da, #e8a0b4);
            border-radius: 40px 40px 40px 0;
            padding: 40px 20px;
            text-align: center;
            min-height: 320px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-shadow: 0 20px 40px rgba(179, 74, 107, 0.15);
            border: 2px dashed #b34a6b;
        }
        .hero-image .emoji-big {
            font-size: 100px;
            line-height: 1;
            margin-bottom: 15px;
        }
        .hero-image .placeholder-text {
            font-size: 18px;
            color: #6b3e4e;
            font-weight: 600;
            background: rgba(255,255,255,0.6);
            padding: 8px 25px;
            border-radius: 60px;
            backdrop-filter: blur(2px);
        }
        .hero-image .sub-placeholder {
            font-size: 14px;
            color: #7a4b5a;
            margin-top: 8px;
        }
        .catalog {
            padding: 70px 0;
            background: #fff9f7;
        }
        .catalog h2 {
            font-family: 'Playfair Display', serif;
            font-size: 38px;
            text-align: center;
            margin-bottom: 15px;
            color: #2d1f1c;
        }
        .catalog .subtitle {
            text-align: center;
            color: #7a5f5a;
            font-size: 18px;
            margin-bottom: 45px;
        }
        .cards {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
            justify-content: center;
        }
        .card {
            background: #ffffff;
            border-radius: 30px;
            padding: 25px 25px 35px;
            flex: 1 1 280px;
            max-width: 340px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.04);
            transition: 0.3s;
            border: 1px solid #f3e1dd;
            text-align: center;
        }
        .card:hover {
            transform: translateY(-12px);
            box-shadow: 0 20px 40px rgba(179, 74, 107, 0.12);
            border-color: #e8a0b4;
        }
        .card-img {
            width: 100%;
            height: 200px;
            background: linear-gradient(145deg, #fce4e0, #f3d0d0);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 70px;
            margin-bottom: 18px;
            border: 1px solid #f8d5da;
        }
        .card h3 {
            font-family: 'Playfair Display', serif;
            font-size: 24px;
            margin-bottom: 8px;
            color: #2d1f1c;
        }
        .card p {
            color: #5f4a46;
            font-size: 15px;
            margin-bottom: 18px;
        }
        .card .price {
            font-weight: 700;
            font-size: 24px;
            color: #b34a6b;
            display: block;
            margin-bottom: 15px;
        }
        .btn-small {
            background: transparent;
            border: 2px solid #b34a6b;
            color: #b34a6b;
            padding: 10px 30px;
            border-radius: 60px;
            font-weight: 600;
            font-size: 15px;
            cursor: pointer;
            transition: 0.3s;
            text-decoration: none;
            display: inline-block;
        }
        .btn-small:hover {
            background: #b34a6b;
            color: #fff;
        }
        .about {
            padding: 70px 0;
            background: #fdf8f5;
        }
        .about .container {
            display: flex;
            gap: 50px;
            align-items: center;
            flex-wrap: wrap;
        }
        .about-text {
            flex: 1 1 50%;
        }
        .about-text h2 {
            font-family: 'Playfair Display', serif;
            font-size: 36px;
            margin-bottom: 20px;
        }
        .about-text p {
            font-size: 18px;
            color: #3d2c2a;
            margin-bottom: 20px;
        }
        .about-image {
            flex: 1 1 40%;
            background: linear-gradient(225deg, #e8a0b4, #f8d5da);
            border-radius: 60px 0 60px 0;
            padding: 50px 20px;
            text-align: center;
            min-height: 250px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            border: 2px dashed #b34a6b;
        }
        .about-image .emoji-big {
            font-size: 80px;
        }
        .footer {
            background: #2d1f1c;
            color: #f0e1dd;
            padding: 40px 0 30px;
        }
        .footer .container {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 30px;
        }
        .footer h4 {
            font-family: 'Playfair Display', serif;
            font-size: 22px;
            margin-bottom: 10px;
            color: #fff;
        }
        .footer p, .footer a {
            color: #d4b9b3;
            text-decoration: none;
            display: block;
            margin-bottom: 6px;
            font-size: 16px;
        }
        .footer a:hover {
            color: #e8a0b4;
        }
        .footer .copy {
            width: 100%;
            text-align: center;
            padding-top: 25px;
            margin-top: 20px;
            border-top: 1px solid #4d3530;
            font-size: 14px;
            color: #8f7370;
        }
        @media (max-width: 768px) {
            .hero-text h1 {
                font-size: 36px;
            }
            .hero .container {
                flex-direction: column;
            }
            .hero-image {
                width: 100%;
                min-height: 200px;
            }
            .header .container {
                flex-direction: column;
                gap: 15px;
            }
            .about .container {
                flex-direction: column;
            }
            .cards {
                flex-direction: column;
                align-items: center;
            }
            .footer .container {
                flex-direction: column;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="container">
            <div class="logo">Зефирный <span>Сад</span></div>
            <a href="tel:+79991234567" class="phone">📞 +7 (926) 408 96 88</a>
        </div>
    </header>
    <section class="hero">
        <div class="container">
            <div class="hero-text">
                <h1>Букеты, которые <span>можно съесть</span></h1>
                <p>Нежные композиции из зефира ручной работы. Идеальный подарок для сладкоежек и романтиков.</p>
                <a href="#catalog" class="btn-primary">Смотреть букеты</a>
            </div>
            <div class="hero-image">
                <div class="emoji-big">🌸🍬</div>
                <div class="placeholder-text">Здесь будет ваше фото букета</div>
            </div>
        </div>
    </section>
    <section class="catalog" id="catalog">
        <div class="container">
            <h2>Наши букеты</h2>
            <p class="subtitle">Собраны вручную из натурального зефира и свежей зелени</p>
            <div class="cards">
                <div class="card">
                    <div class="card-img">🌷🌸</div>
                    <h3>Нежный сад</h3>
                    <p>9 цветков зефира, пастельные тона, веточки мяты.</p>
                    <span class="price">2 990 ₽</span>
                    <button class="btn-small">Заказать</button>
                </div>
                <div class="card">
                    <div class="card-img">🍓🌿</div>
                    <h3>Ягодное настроение</h3>
                    <p>Зефир с начинкой из ягодного конфи, 11 штук.</p>
                    <span class="price">3 490 ₽</span>
                    <button class="btn-small">Заказать</button>
                </div>
                <div class="card">
                    <div class="card-img">💐🍭</div>
                    <h3>Зефирный пир</h3>
                    <p>Большой букет (15 шт) с декором из сухоцветов.</p>
                    <span class="price">4 990 ₽</span>
                    <button class="btn-small">Заказать</button>
                </div>
            </div>
        </div>
    </section>
    <section class="about">
        <div class="container">
            <div class="about-text">
                <h2>ИП «СЛАВИНСКАЯ МАРИНА ВАСИЛЬЕВНА»</h2>
                <p>Мы делаем букеты, которые дарят эмоции и вкус. Каждый зефир готовится по домашнему рецепту, а композиции собираются с любовью.</p>
                <p>Доставляем по городу в день заказа. Съедобные букеты — это наш ответ скучным подаркам.</p>
            </div>
            <div class="about-image">
                <div class="emoji-big">🧁✨</div>
                <div class="placeholder-text">Фото производства / основателя</div>
            </div>
        </div>
    </section>
    <footer class="footer">
        <div class="container">
            <div>
                <h4>Зефирный Сад</h4>
                <p>ИП СЛАВИНСКАЯ МАРИНА ВАСИЛЬЕВНА</p>
                <p>ОГРНИП: 326508100376034</p>
            </div>
            <div>
                <h4>Контакты</h4>
                <a href="tel:+79991234567">+7 (926) 408-96-88</a>
                <a href="https://www.instagram.com/vkusniydom_/">@Vkusniydom_.ru</a>
                <p>г. Москва, ул. Хуторская 2-я, д. 38А, стр. 26</p>
            </div>
            <div>
                <h4>Режим работы</h4>
                <p>Ежедневно: 10:00 – 20:00</p>
                <p>Доставка с 11:00 до 22:00</p>
            </div>
            <div class="copy">
                © 2026 ИП СЛАВИНСКАЯ МАРИНА ВАСИЛЬЕВНА. Все права защищены.
            </div>
        </div>
    </footer>
    <script>
        document.querySelectorAll('.btn-small').forEach(btn => {
            btn.addEventListener('click', function(e) {
                e.preventDefault();
                alert('Спасибо! Мы свяжемся с вами для оформления заказа.');
            });
        });
    </script>
</body>
</html>
