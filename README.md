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
                        url('https://images.unsplash.com/photo-1538481199705-c710c4e965fc?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            height: 100vh;
            display: flex;
            flex-direction: column;
            background-size: cover;
            background-position: center;
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

        /* Оборудование */
        .equipment {
            padding: 5rem 5%;
            text-align: center;
            background: #000;
        }

        .equipment-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .equipment-card {
            background: rgba(255,255,255,0.05);
            padding: 2rem;
            border-radius: 10px;
            transition: 0.3s;
        }

        .equipment-card:hover {
            transform: translateY(-5px);
        }

        .equipment-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 5px;
            margin-bottom: 1rem;
        }

        /* Остальные стили из предыдущего кода... */
        /* (Все остальные секции и стили остаются без изменений) */

        @media (max-width: 768px) {
            .equipment-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <nav class="nav">
            <a href="#" class="logo">CyberCore</a>
            <div class="nav-links">
                <a href="#equipment">Оборудование</a>
                <a href="#zones">Зоны</a>
                <a href="#pricing">Тарифы</a>
                <a href="#contact">Контакты</a>
            </div>
        </nav>

        <section class="hero">
            <div class="hero-content">
                <h1>Погрузитесь в мир игр</h1>
                <p>20 игровых ПК • 4 консоли • 4 VR-шлема</p>
                <button class="btn" style="margin-top: 2rem;">Забронировать место</button>
            </div>
        </section>
    </header>

    <!-- Секция с оборудованием -->
    <section class="equipment" id="equipment">
        <h2>Наше оборудование</h2>
        <div class="equipment-grid">
            <div class="equipment-card">
                <img src="https://images.unsplash.com/photo-1593640408182-31c228c7fcb8?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80" alt="Игровые ПК">
                <h3>20 Игровых ПК</h3>
                <ul style="text-align: left; list-style: none;">
                    <li>► Intel Core i9-13900K</li>
                    <li>► NVIDIA RTX 4090</li>
                    <li>► 32GB DDR5 RAM</li>
                    <li>► 1TB NVMe SSD</li>
                </ul>
            </div>

            <div class="equipment-card">
                <img src="https://images.unsplash.com/photo-1606144042614-b2417e99c4e3?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80" alt="Игровые приставки">
                <h3>4 Консольные зоны</h3>
                <ul style="text-align: left; list-style: none;">
                    <li>► PlayStation 5</li>
                    <li>► Xbox Series X</li>
                    <li>► Nintendo Switch</li>
                    <li>► 4K HDR Телевизоры</li>
                </ul>
            </div>

            <div class="equipment-card">
                <img src="https://images.unsplash.com/photo-1586227747543-50a2fc446640?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80" alt="VR-оборудование">
                <h3>4 VR-станции</h3>
                <ul style="text-align: left; list-style: none;">
                    <li>► Meta Quest 3</li>
                    <li>► Valve Index</li>
                    <li>► HTC Vive Pro 2</li>
                    <li>► Специальные контроллеры</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Остальные секции (зоны, форма бронирования) -->
    <!-- ... (остальной код из предыдущего ответа без изменений) ... -->

    <script>
        // Обновленный скрипт для бронирования с учетом оборудования
        document.getElementById('bookingForm').addEventListener('submit', (e) => {
            e.preventDefault();
            
            const equipmentType = document.querySelector('select').value;
            const message = `Забронирована ${equipmentType}. Ожидайте подтверждения!`;
            
            alert(message);
            e.target.reset();
        });

        // Анимации
        const cards = document.querySelectorAll('.equipment-card');
        cards.forEach((card, index) => {
            card.style.transitionDelay = `${index * 100}ms`;
        });
    </script>
</body>
</html>
        });
    </script>
</body>
</html>
