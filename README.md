<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CyberCore Gaming Club</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', sans-serif;
        }

        :root {
            --primary-color: #6c5ce7;
            --dark-bg: #2d3436;
            --neon-blue: #00f3ff;
        }

        body {
            background-color: var(--dark-bg);
            color: white;
        }

        /* Header */
        .header {
            background: linear-gradient(rgba(0,0,0,0.9), rgba(0,0,0,0.9)),
                        url('gaming-bg.jpg') center/cover;
            height: 100vh;
            display: flex;
            flex-direction: column;
        }

        .nav {
            padding: 1.5rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 2rem;
            color: var(--neon-blue);
            text-decoration: none;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--neon-blue);
        }

        /* Hero Section */
        .hero {
            flex: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        .hero-content h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #00f3ff, #6c5ce7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Features Section */
        .features {
            padding: 5rem 5%;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            background: #000;
        }

        .feature-card {
            background: rgba(255,255,255,0.05);
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            transition: 0.3s;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            background: rgba(255,255,255,0.1);
        }

        /* Gaming Zones Section */
        .zones {
            padding: 5rem 5%;
        }

        .zone-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .zone-card {
            position: relative;
            overflow: hidden;
            border-radius: 15px;
        }

        .zone-card img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            transition: 0.3s;
        }

        .zone-card:hover img {
            transform: scale(1.1);
        }

        /* Booking Form */
        .booking-form {
            background: #000;
            padding: 5rem 5%;
            text-align: center;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        input, select {
            width: 100%;
            max-width: 400px;
            padding: 1rem;
            background: rgba(255,255,255,0.1);
            border: 1px solid var(--neon-blue);
            color: white;
            border-radius: 5px;
        }

        .btn {
            background: var(--primary-color);
            color: white;
            padding: 1rem 2rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn:hover {
            background: #5b4bc4;
        }

        /* Адаптивность */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .zone-grid {
                grid-template-columns: 1fr;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <nav class="nav">
            <a href="#" class="logo">CyberCore</a>
            <div class="nav-links">
                <a href="#about">О нас</a>
                <a href="#zones">Зоны</a>
                <a href="#pricing">Тарифы</a>
                <a href="#contact">Контакты</a>
            </div>
        </nav>

        <!-- Hero Section -->
        <section class="hero">
            <div class="hero-content">
                <h1>Погрузитесь в мир игр</h1>
                <p>Лучшее оборудование • Киберспортивные турниры • Комфортные зоны</p>
                <button class="btn" style="margin-top: 2rem;">Забронировать место</button>
            </div>
        </section>
    </header>

    <!-- Features -->
    <section class="features">
        <div class="feature-card">
            <i class="fas fa-tachometer-alt fa-3x"></i>
            <h3>Мощные ПК</h3>
            <p>RTX 4090 • Intel i9 • 32GB RAM</p>
        </div>
        <div class="feature-card">
            <i class="fas fa-coffee fa-3x"></i>
            <h3>Комфорт</h3>
            <p>Эргономичные кресла • Бары • Зоны отдыха</p>
        </div>
        <div class="feature-card">
            <i class="fas fa-trophy fa-3x"></i>
            <h3>Турниры</h3>
            <p>Еженедельные соревнования с призами</p>
        </div>
    </section>

    <!-- Gaming Zones -->
    <section class="zones" id="zones">
        <h2 style="text-align: center;">Наши игровые зоны</h2>
        <div class="zone-grid">
            <div class="zone-card">
                <img src="gaming-zone1.jpg" alt="VR Zone">
                <div class="zone-info">
                    <h3>VR-арена</h3>
                </div>
            </div>
            <div class="zone-card">
                <img src="gaming-zone2.jpg" alt="PC Zone">
                <div class="zone-info">
                    <h3>Премиум ПК</h3>
                </div>
            </div>
            <div class="zone-card">
                <img src="gaming-zone3.jpg" alt="Console Zone">
                <div class="zone-info">
                    <h3>Консольная зона</h3>
                </div>
            </div>
        </div>
    </section>

    <!-- Booking Form -->
    <section class="booking-form">
        <h2>Забронировать место</h2>
        <form id="bookingForm">
            <div class="form-group">
                <input type="text" placeholder="Азиз" required>
            </div>
            <div class="form-group">
                <input type="email" placeholder="aziz.saliv.01@gmail.com" required>
            </div>
            <div class="form-group">
                <select required>
                    <option value="">Выберите зону</option>
                    <option>VR-арена</option>
                    <option>Премиум ПК</option>
                    <option>Консольная зона</option>
                </select>
            </div>
            <button type="submit" class="btn">Отправить</button>
        </form>
    </section>

    <script>
        // Анимации при скролле
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('show');
                }
            });
        });

        document.querySelectorAll('.feature-card, .zone-card').forEach((el) => {
            observer.observe(el);
        });

        // Обработка формы
        document.getElementById('bookingForm').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Заявка отправлена! Мы свяжемся с вами в ближайшее время.');
            e.target.reset();
        });
    </script>
</body>
</html>
