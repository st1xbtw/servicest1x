<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>st1xlox Services</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --dark-blue: #1a1a2e;
            --dark-blue-2: #16213e;
            --blue: #0f3460;
            --purple: #533483;
            --accent: #e94560;
            --neon-purple: #b967ff;
            --neon-pink: #ff2a6d;
            --neon-cyan: #00f3ff;
            --bg-primary: #0f0f23;
            --bg-secondary: #1a1a2e;
            --text-primary: #ffffff;
            --text-secondary: #e0e0e0;
            --card-bg: rgba(255, 255, 255, 0.08);
            --card-border: rgba(255, 255, 255, 0.15);
            --shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.36);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            transition: background-color 0.3s, color 0.3s, border-color 0.3s;
        }

        body {
            background: var(--bg-primary);
            color: var(--text-primary);
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            min-height: 100vh;
            overflow-x: hidden;
            padding-top: 76px;
        }

        /* Анимированный фон */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }

        .bg-animation::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(83, 52, 131, 0.1) 0%, rgba(26, 26, 46, 0) 70%);
            animation: pulse 15s infinite linear;
        }

        @keyframes pulse {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }

        /* Анимированные шары для главной страницы */
        .ball {
            position: absolute;
            border-radius: 50%;
            background: rgba(179, 103, 255, 0.2);
            animation: float 15s infinite linear;
            z-index: -1;
        }

        .ball-1 { width: 100px; height: 100px; top: 10%; left: 10%; }
        .ball-2 { width: 150px; height: 150px; top: 50%; left: 50%; }
        .ball-3 { width: 200px; height: 200px; top: 80%; left: 80%; }

        @keyframes float {
            0% { transform: translate(0, 0) rotate(0deg); }
            50% { transform: translate(100px, 100px) rotate(180deg); }
            100% { transform: translate(0, 0) rotate(360deg); }
        }

        /* Glassmorphism стили */
        .glass-card {
            background: var(--card-bg);
            backdrop-filter: blur(12px);
            border-radius: 20px;
            border: 1px solid var(--card-border);
            box-shadow: var(--shadow);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            overflow: hidden;
            position: relative;
        }

        .glass-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--neon-purple), transparent);
        }

        .glass-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 40px 0 rgba(0, 0, 0, 0.5), 0 0 20px rgba(179, 103, 255, 0.3);
            border-color: rgba(179, 103, 255, 0.4);
        }

        .glass-card-static {
            background: var(--card-bg);
            backdrop-filter: blur(12px);
            border-radius: 20px;
            border: 1px solid var(--card-border);
            box-shadow: var(--shadow);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            overflow: hidden;
            position: relative;
        }

        .glass-card-static::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--neon-purple), transparent);
        }

        .glass-card-static:hover {
            box-shadow: 0 15px 40px 0 rgba(0, 0, 0, 0.5), 0 0 20px rgba(179, 103, 255, 0.3);
            border-color: rgba(179, 103, 255, 0.4);
        }

        /* Кнопки */
        .btn-primary {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            border: none;
            border-radius: 12px;
            padding: 12px 30px;
            font-weight: 600;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(83, 52, 131, 0.4);
            color: white;
        }

        .btn-primary::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(83, 52, 131, 0.6);
            color: white;
        }

        .btn-primary:hover::before {
            left: 100%;
        }

        .btn-accent {
            background: linear-gradient(135deg, var(--accent), var(--neon-pink));
            border: none;
            border-radius: 12px;
            padding: 12px 30px;
            font-weight: 600;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(233, 69, 96, 0.4);
            color: white;
        }

        .btn-accent::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }

        .btn-accent:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(233, 69, 96, 0.6);
            color: white;
        }

        .btn-accent:hover::before {
            left: 100%;
        }

        /* Навигация */
        .navbar {
            background: rgba(26, 26, 46, 0.95) !important;
            backdrop-filter: blur(15px);
            border-bottom: 1px solid rgba(83, 52, 131, 0.3);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
        }

        .navbar-brand, .nav-link {
            color: var(--text-primary) !important;
            transition: color 0.3s ease;
            position: relative;
        }

        .nav-link::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, var(--neon-purple), var(--neon-pink));
            transition: width 0.3s ease;
        }

        .nav-link:hover::after {
            width: 100%;
        }

        .nav-link:hover {
            color: var(--neon-purple) !important;
        }

        /* Герой секция */
        .hero-section {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(26, 26, 46, 0.9), rgba(22, 33, 62, 0.9));
            background-size: cover;
            background-position: center;
            z-index: -1;
        }

        .hero-content {
            position: relative;
            z-index: 1;
        }

        .floating-element {
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-20px);
            }
            100% {
                transform: translateY(0px);
            }
        }

        /* Страницы */
        .page {
            display: none;
            animation: fadeIn 0.5s ease;
        }

        .active-page {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Формы */
        .form-control {
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: var(--text-primary);
            border-radius: 12px;
            padding: 12px 15px;
            transition: all 0.3s ease;
        }

        .form-control:focus {
            background: rgba(255, 255, 255, 0.15);
            border-color: var(--neon-purple);
            box-shadow: 0 0 0 0.25rem rgba(83, 52, 131, 0.25);
            color: var(--text-primary);
        }

        .form-label {
            color: var(--text-primary);
            font-weight: 500;
        }

        /* НОВЫЙ СТИЛЬ: ИНТЕРАКТИВНЫЙ КОНСТРУКТОР ЗАКАЗОВ */
        .order-constructor {
            max-width: 1000px;
            margin: 0 auto;
        }

        .constructor-steps {
            display: flex;
            justify-content: space-between;
            margin-bottom: 40px;
            position: relative;
        }

        .constructor-steps::before {
            content: '';
            position: absolute;
            top: 20px;
            left: 0;
            right: 0;
            height: 3px;
            background: rgba(255, 255, 255, 0.1);
            z-index: 1;
        }

        .step-indicator {
            position: relative;
            z-index: 2;
            text-align: center;
            flex: 1;
        }

        .step-circle {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 10px;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .step-indicator.active .step-circle {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            border-color: var(--neon-purple);
            box-shadow: 0 0 15px rgba(179, 103, 255, 0.5);
        }

        .step-indicator.completed .step-circle {
            background: linear-gradient(135deg, var(--accent), var(--neon-pink));
        }

        .step-content {
            display: none;
        }

        .step-content.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }

        .service-visual-preview {
            height: 200px;
            border-radius: 15px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            position: relative;
            overflow: hidden;
        }

        .service-visual-preview::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grid" width="10" height="10" patternUnits="userSpaceOnUse"><path d="M 10 0 L 0 0 0 10" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="0.5"/></pattern></defs><rect width="100" height="100" fill="url(%23grid)"/></svg>');
        }

        .service-options-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 30px;
        }

        .service-option-card {
            background: var(--card-bg);
            border: 2px solid transparent;
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .service-option-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(179, 103, 255, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .service-option-card:hover::before {
            left: 100%;
        }

        .service-option-card:hover,
        .service-option-card.active {
            transform: translateY(-5px);
            border-color: var(--neon-purple);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .service-icon {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .option-features {
            list-style: none;
            padding: 0;
            margin: 15px 0;
            text-align: left;
        }

        .option-features li {
            padding: 5px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
        }

        .option-features li:last-child {
            border-bottom: none;
        }

        .option-features li::before {
            content: '✓';
            color: var(--neon-purple);
            margin-right: 8px;
            font-weight: bold;
        }

        .customization-options {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .customization-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            transition: all 0.3s ease;
        }

        .customization-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.08);
        }

        .customization-preview {
            width: 100%;
            height: 150px;
            border-radius: 10px;
            background: rgba(0, 0, 0, 0.2);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .preview-animation {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: conic-gradient(var(--neon-purple), var(--neon-pink), var(--neon-purple));
            animation: rotate 3s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .constructor-navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 30px;
        }

        .order-summary-preview {
            position: sticky;
            top: 100px;
            background: var(--card-bg);
            border-radius: 20px;
            padding: 25px;
            border: 1px solid var(--card-border);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .summary-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            padding-bottom: 10px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .summary-total {
            font-size: 1.3rem;
            font-weight: bold;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 2px solid rgba(255, 255, 255, 0.2);
        }

        .floating-badge {
            position: absolute;
            top: -10px;
            right: -10px;
            background: linear-gradient(135deg, var(--accent), var(--neon-pink));
            color: white;
            border-radius: 20px;
            padding: 5px 12px;
            font-size: 0.8rem;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(233, 69, 96, 0.4);
        }

        /* Анимации */
        .pulse {
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(179, 103, 255, 0.7);
            }
            70% {
                box-shadow: 0 0 0 15px rgba(179, 103, 255, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(179, 103, 255, 0);
            }
        }

        .floating {
            animation: floating 3s ease-in-out infinite;
        }

        @keyframes floating {
            0% { transform: translate(0, 0px); }
            50% { transform: translate(0, -15px); }
            100% { transform: translate(0, -0px); }
        }

        /* Адаптивность */
        @media (max-width: 768px) {
            .constructor-steps {
                flex-direction: column;
                gap: 20px;
            }

            .constructor-steps::before {
                display: none;
            }

            .service-options-grid {
                grid-template-columns: 1fr;
            }

            .customization-options {
                grid-template-columns: 1fr;
            }

            .constructor-navigation {
                flex-direction: column;
                gap: 10px;
            }
            
            .hero-cta-buttons {
                flex-direction: column;
            }
            
            .hero-feature-grid {
                grid-template-columns: 1fr;
            }
            
            .reviews-grid {
                grid-template-columns: 1fr;
            }
            
            .profile-stats-modern {
                grid-template-columns: 1fr;
            }
            
            .profile-actions-modern {
                flex-direction: column;
            }
            
            .asymmetric-profile {
                grid-template-columns: 1fr;
            }
            
            .admin-dashboard {
                grid-template-columns: 1fr;
            }
            
            .admin-quick-actions {
                grid-template-columns: 1fr;
            }
            
            .navbar-collapse {
                background: var(--bg-secondary);
                padding: 15px;
                border-radius: 10px;
                margin-top: 10px;
            }
            
            .hero-section {
                min-height: auto;
                padding: 100px 0 50px;
            }
            
            .display-4 {
                font-size: 2rem;
            }
            
            .container {
                padding-left: 15px;
                padding-right: 15px;
            }
        }

        /* Улучшенный AI чат */
        .ai-response-variations {
            font-style: italic;
            opacity: 0.8;
            margin-top: 10px;
            padding: 10px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            border-left: 3px solid var(--neon-purple);
        }

        /* Стили для звездного рейтинга */
        .stars-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 30px;
            color: var(--text-primary);
        }

        .stars-visual {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }

        .star-visual {
            font-size: 3rem;
            color: #ffd700;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
            animation: twinkle 2s infinite alternate;
        }

        @keyframes twinkle {
            0% { transform: scale(1); opacity: 0.7; }
            100% { transform: scale(1.1); opacity: 1; }
        }

        .star-visual:nth-child(2) { animation-delay: 0.2s; }
        .star-visual:nth-child(3) { animation-delay: 0.4s; }
        .star-visual:nth-child(4) { animation-delay: 0.6s; }
        .star-visual:nth-child(5) { animation-delay: 0.8s; }

        /* Система уведомлений */
        .notification-system {
            position: fixed;
            top: 100px;
            right: 20px;
            z-index: 1000;
        }

        .notification-item {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            color: white;
            padding: 15px 20px;
            border-radius: 12px;
            margin-bottom: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transform: translateX(150%);
            transition: transform 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            max-width: 300px;
        }

        .notification-item.show {
            transform: translateX(0);
        }

        .notification-item.success {
            background: linear-gradient(135deg, #28a745, #20c997);
        }

        .notification-item.error {
            background: linear-gradient(135deg, #dc3545, #e83e8c);
        }

        .notification-item.warning {
            background: linear-gradient(135deg, #ffc107, #fd7e14);
        }

        /* Стили для отзывов без анимации */
        .review-card {
            max-width: 100%;
            word-wrap: break-word;
            overflow-wrap: break-word;
            transition: none !important;
        }

        .review-card:hover {
            transform: none !important;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.36) !important;
            border-color: rgba(255, 255, 255, 0.15) !important;
        }

        .review-text {
            white-space: pre-line;
            word-break: break-word;
            line-height: 1.5;
            margin-bottom: 10px;
        }

        .review-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
            flex-wrap: wrap;
            gap: 10px;
        }

        .review-author {
            font-weight: bold;
            font-size: 1.1rem;
        }

        .review-date {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .review-rating {
            margin-top: 10px;
            display: flex;
            justify-content: center;
        }

        .carousel-item .glass-card {
            min-height: 200px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        /* Стили для улучшенной админ-панели */
        .admin-stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .admin-stat-card {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .admin-stat-card:hover {
            transform: translateY(-5px);
        }

        .admin-stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .admin-stat-label {
            font-size: 1rem;
            opacity: 0.9;
        }

        .admin-chart-container {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            margin-bottom: 30px;
        }

        .admin-filter-bar {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 20px;
        }

        .ai-bot-message {
            background: linear-gradient(135deg, var(--blue), var(--purple));
            border-radius: 15px;
            padding: 15px;
            margin: 10px 0;
            position: relative;
        }

        .ai-bot-message::before {
            content: '🤖';
            position: absolute;
            left: -30px;
            top: 15px;
            font-size: 1.2rem;
        }

        .typing-indicator {
            display: inline-block;
            padding: 10px 15px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            margin: 5px 0;
        }

        .typing-dots {
            display: inline-block;
        }

        .typing-dots span {
            animation: typing 1.4s infinite;
            display: inline-block;
        }

        .typing-dots span:nth-child(2) {
            animation-delay: 0.2s;
        }

        .typing-dots span:nth-child(3) {
            animation-delay: 0.4s;
        }

        @keyframes typing {
            0%, 60%, 100% { transform: translateY(0); }
            30% { transform: translateY(-5px); }
        }

        .quick-replies {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }

        .quick-reply {
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            padding: 8px 15px;
            font-size: 0.9rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .quick-reply:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-2px);
        }

        /* Улучшенный личный кабинет */
        .dashboard-container {
            padding: 0;
        }

        .dashboard-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 25px;
        }

        .dashboard-stat {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .dashboard-stat:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.08);
        }

        .dashboard-stat-number {
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 5px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .dashboard-stat-label {
            font-size: 0.9rem;
            opacity: 0.8;
        }

        .profile-header {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
        }

        .profile-actions {
            display: flex;
            gap: 10px;
            margin-top: 15px;
        }

        .profile-details {
            flex: 1;
            margin-left: 20px;
        }

        .activity-timeline {
            margin-top: 25px;
        }

        .timeline-item {
            display: flex;
            margin-bottom: 15px;
            position: relative;
        }

        .timeline-item:before {
            content: '';
            position: absolute;
            left: 20px;
            top: 0;
            bottom: -15px;
            width: 2px;
            background: var(--purple);
        }

        .timeline-item:last-child:before {
            display: none;
        }

        .timeline-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--purple);
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            z-index: 1;
        }

        .timeline-content {
            flex: 1;
        }

        .timeline-date {
            font-size: 0.8rem;
            opacity: 0.7;
            margin-bottom: 5px;
        }

        /* Анимация для звезд рейтинга */
        .star-rating {
            display: flex;
            gap: 5px;
        }

        .star {
            font-size: 24px;
            color: #444;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .star:hover {
            transform: scale(1.2);
        }

        .star.active {
            color: #ffc107;
            text-shadow: 0 0 10px rgba(255, 193, 7, 0.7);
        }

        .star.hover {
            color: #ffc107;
            text-shadow: 0 0 15px rgba(255, 193, 7, 0.9);
        }

        /* Новые стили для улучшенных блоков услуг */
        .modern-service-card {
            border-radius: 20px;
            overflow: hidden;
            transition: all 0.3s ease;
            height: 100%;
        }

        .modern-service-card:hover {
            transform: translateY(-10px);
        }

        .service-icon {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 1.8rem;
        }

        .service-icon.telegram {
            background: linear-gradient(135deg, #0088cc, #34b7f1);
        }

        .service-icon.stars {
            background: linear-gradient(135deg, #ffd700, #ffed4e);
        }

        .service-icon.support {
            background: linear-gradient(135deg, var(--accent), var(--neon-pink));
        }

        .step-by-step {
            counter-reset: step;
            color: var(--text-primary);
        }

        .step-item {
            display: flex;
            margin-bottom: 20px;
            align-items: flex-start;
        }

        .step-number {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-right: 15px;
            flex-shrink: 0;
        }

        .step-content {
            flex: 1;
        }

        .step-content h6 {
            margin-bottom: 5px;
            font-weight: 600;
        }

        .step-content p {
            margin: 0;
            opacity: 0.8;
        }

        /* Стили для нового AI-чата */
        .ultra-ai-message {
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            border-radius: 15px;
            padding: 15px;
            margin: 10px 0;
            position: relative;
            border: 1px solid rgba(179, 103, 255, 0.3);
        }

        .ultra-ai-message::before {
            content: '🧠';
            position: absolute;
            left: -30px;
            top: 15px;
            font-size: 1.2rem;
        }

        .ai-thinking {
            font-style: italic;
            opacity: 0.7;
            margin-top: 5px;
            font-size: 0.9rem;
        }

        /* Улучшенная админ-панель */
        .admin-dashboard {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .admin-widget {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            transition: all 0.3s ease;
        }

        .admin-widget:hover {
            background: rgba(255, 255, 255, 0.08);
            transform: translateY(-5px);
        }

        .admin-widget-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .admin-widget-title {
            font-size: 1.2rem;
            font-weight: 600;
        }

        .admin-widget-value {
            font-size: 2rem;
            font-weight: bold;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .admin-widget-chart {
            height: 100px;
            margin-top: 15px;
        }

        .admin-action-buttons {
            display: flex;
            gap: 10px;
            margin-top: 15px;
        }

        .admin-table-container {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            margin-bottom: 20px;
        }

        .admin-table-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }

        .admin-search-box {
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            padding: 8px 15px;
            color: var(--text-primary);
            width: 250px;
        }

        .admin-search-box::placeholder {
            color: var(--text-secondary);
        }

        /* НОВЫЕ СТИЛИ ДЛЯ АДМИН-ПАНЕЛИ */
        .admin-action-btn {
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: var(--text-primary);
            border-radius: 8px;
            padding: 8px 15px;
            transition: all 0.3s ease;
            font-size: 0.9rem;
        }

        .admin-action-btn:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-2px);
        }

        /* НОВЫЕ СТИЛИ ДЛЯ ЛИЧНОГО КАБИНЕТА */
        .recent-activity {
            margin-top: 25px;
        }

        .activity-item {
            display: flex;
            align-items: center;
            padding: 12px 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            margin-bottom: 10px;
            transition: all 0.3s ease;
        }

        .activity-item:hover {
            background: rgba(255, 255, 255, 0.08);
            transform: translateX(5px);
        }

        .activity-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--purple);
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-size: 1.2rem;
        }

        .activity-content {
            flex: 1;
        }

        .activity-title {
            font-weight: 600;
            margin-bottom: 5px;
        }

        .activity-time {
            font-size: 0.8rem;
            color: var(--text-secondary);
        }

        /* НОВЫЕ СТИЛИ ДЛЯ СОВРЕМЕННОГО ОФОРМЛЕНИЯ ЗАКАЗА */
        .modern-order-tabs {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .modern-tab {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 20px;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .modern-tab::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(179, 103, 255, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .modern-tab:hover::before {
            left: 100%;
        }

        .modern-tab.active {
            background: rgba(179, 103, 255, 0.1);
            border-color: var(--neon-purple);
            box-shadow: 0 5px 20px rgba(179, 103, 255, 0.2);
        }

        .modern-tab:hover {
            transform: translateY(-3px);
            border-color: rgba(179, 103, 255, 0.3);
        }

        .tab-header {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .tab-icon {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-size: 1.5rem;
        }

        .tab-title {
            font-size: 1.3rem;
            font-weight: 600;
        }

        .tab-description {
            color: var(--text-secondary);
            margin-bottom: 15px;
        }

        .tab-features {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }

        .feature-tag {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 5px 12px;
            font-size: 0.8rem;
        }

        .order-preview {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            margin-top: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .preview-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .preview-title {
            font-size: 1.2rem;
            font-weight: 600;
        }

        .preview-price {
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: bold;
            font-size: 1.3rem;
        }

        .preview-image {
            width: 100%;
            border-radius: 10px;
            margin: 15px 0;
            background: rgba(255, 255, 255, 0.05);
            height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: rgba(255, 255, 255, 0.3);
        }

        .floating-order-card {
            position: sticky;
            top: 100px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .order-summary {
            margin-bottom: 20px;
        }

        .summary-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            padding-bottom: 10px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .summary-total {
            font-size: 1.3rem;
            font-weight: bold;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 2px solid rgba(255, 255, 255, 0.2);
        }

        .floating-badge {
            position: absolute;
            top: -10px;
            right: -10px;
            background: linear-gradient(135deg, var(--accent), var(--neon-pink));
            color: white;
            border-radius: 20px;
            padding: 5px 12px;
            font-size: 0.8rem;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(233, 69, 96, 0.4);
        }
        
        /* Новые стили для улучшенного главного меню */
        .hero-animated-text {
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink), #ffd700, #00ff88);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient 5s ease infinite;
        }
        
        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .hero-subtitle {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            background: linear-gradient(135deg, var(--text-primary), var(--text-secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .hero-cta-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }
        
        .hero-feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 50px;
        }
        
        .hero-feature-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .hero-feature-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .hero-feature-icon {
            font-size: 3rem;
            margin-bottom: 15px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        /* Улучшенный AI чат */
        .ai-response-variations {
            font-style: italic;
            opacity: 0.8;
            margin-top: 10px;
            padding: 10px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            border-left: 3px solid var(--neon-purple);
        }
        
        /* Улучшенный личный кабинет */
        .profile-completion {
            margin-top: 20px;
            padding: 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
        }
        
        .completion-bar {
            height: 8px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            margin-top: 10px;
            overflow: hidden;
        }
        
        .completion-progress {
            height: 100%;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            border-radius: 4px;
            width: 65%;
        }
        
        .profile-badges {
            display: flex;
            gap: 10px;
            margin-top: 15px;
            flex-wrap: wrap;
        }
        
        .profile-badge {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 5px 12px;
            font-size: 0.8rem;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        /* Улучшенная админ-панель */
        .admin-quick-actions {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 30px;
        }
        
        .admin-quick-action {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .admin-quick-action:hover {
            background: rgba(255, 255, 255, 0.08);
            transform: translateY(-5px);
        }
        
        .admin-quick-action-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        /* Стили для видео в заказах */
        .video-preview {
            width: 100%;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            background: #000;
        }
        
        .video-preview video {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .video-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .video-preview:hover .video-overlay {
            opacity: 1;
        }
        
        .play-button {
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.8);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #000;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Новые стили для звездного рейтинга */
        .stars-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 30px;
        }
        
        .stars-visual {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .star-visual {
            font-size: 3rem;
            color: #ffd700;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
            animation: twinkle 2s infinite alternate;
        }
        
        @keyframes twinkle {
            0% { transform: scale(1); opacity: 0.7; }
            100% { transform: scale(1.1); opacity: 1; }
        }
        
        .star-visual:nth-child(2) { animation-delay: 0.2s; }
        .star-visual:nth-child(3) { animation-delay: 0.4s; }
        .star-visual:nth-child(4) { animation-delay: 0.6s; }
        .star-visual:nth-child(5) { animation-delay: 0.8s; }
        
        /* Стили для галереи работ */
        .portfolio-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .portfolio-item {
            position: relative;
            border-radius: 15px;
            overflow: hidden;
            height: 200px;
            transition: transform 0.3s ease;
        }
        
        .portfolio-item:hover {
            transform: translateY(-5px);
        }
        
        .portfolio-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.7);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }
        
        .portfolio-title {
            color: white;
            font-weight: bold;
            text-align: center;
            padding: 10px;
        }
        
        /* Стили для карусели заказов */
        .order-carousel {
            display: flex;
            overflow-x: auto;
            gap: 20px;
            padding: 20px 0;
            scroll-behavior: smooth;
        }
        
        .order-carousel-item {
            flex: 0 0 auto;
            width: 300px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.3s ease;
        }
        
        .order-carousel-item:hover {
            transform: translateY(-5px);
        }
        
        .carousel-item-image {
            width: 100%;
            height: 150px;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: white;
        }
        
        .carousel-item-content {
            padding: 15px;
        }
        
        .carousel-item-title {
            font-size: 1.2rem;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .carousel-item-price {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--neon-purple);
            margin-bottom: 10px;
        }
        
        .carousel-item-features {
            list-style: none;
            padding: 0;
            margin-bottom: 15px;
        }
        
        .carousel-item-features li {
            padding: 5px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .carousel-item-features li:last-child {
            border-bottom: none;
        }
        
        /* Стили для страницы "О нас" */
        .about-hero {
            min-height: 60vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, rgba(26, 26, 46, 0.9), rgba(22, 33, 62, 0.9));
            position: relative;
            overflow: hidden;
        }
        
        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .team-member {
            text-align: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            transition: transform 0.3s ease;
        }
        
        .team-member:hover {
            transform: translateY(-10px);
        }
        
        .team-member-avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            margin: 0 auto 15px;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            color: white;
        }
        
        .team-member-name {
            font-size: 1.3rem;
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .team-member-role {
            color: var(--neon-purple);
            margin-bottom: 15px;
        }
        
        .stats-counter {
            display: flex;
            justify-content: space-around;
            margin: 50px 0;
            text-align: center;
        }
        
        .stat-item {
            padding: 20px;
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }
        
        .stat-label {
            font-size: 1.1rem;
            opacity: 0.8;
        }

        /* НОВЫЕ СТИЛИ ДЛЯ УЛУЧШЕННОЙ ГЛАВНОЙ СТРАНИЦЫ */
        .feature-card-icon {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 2rem;
        }

        /* НОВЫЕ СТИЛИ ДЛЯ УЛУЧШЕННОЙ СТРАНИЦЫ О НАС */
        .about-telegram-section {
            padding: 50px 0;
        }

        .telegram-channel-card, .telegram-chat-card {
            border-radius: 15px;
            overflow: hidden;
            margin-bottom: 30px;
        }

        .telegram-channel-header {
            background: #0088cc;
            color: white;
            padding: 15px 20px;
            display: flex;
            align-items: center;
        }

        .telegram-channel-content {
            padding: 20px;
            background: white;
            color: #333;
        }

        .telegram-channel-message {
            background: #e8f4f9;
            border-radius: 12px;
            padding: 12px 15px;
            margin-bottom: 10px;
            position: relative;
        }

        .telegram-channel-message:after {
            content: '';
            position: absolute;
            left: -10px;
            top: 10px;
            width: 0;
            height: 0;
            border: 10px solid transparent;
            border-right-color: #e8f4f9;
        }

        .telegram-chat-header {
            background: #5682a3;
            color: white;
            padding: 15px 20px;
            display: flex;
            align-items: center;
        }

        .telegram-chat-content {
            padding: 20px;
            background: white;
            color: #333;
        }

        .telegram-chat-message {
            display: flex;
            margin-bottom: 15px;
        }

        .telegram-chat-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--purple);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            margin-right: 10px;
            flex-shrink: 0;
        }

        .telegram-chat-text {
            background: #e8f4f9;
            border-radius: 12px;
            padding: 10px 15px;
            max-width: 80%;
        }

        .contact-admin-section {
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            margin-top: 30px;
        }

        /* НОВЫЕ СТИЛИ ДЛЯ УЛУЧШЕННОЙ СТРАНИЦЫ ОТЗЫВОВ */
        .reviews-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .review-item-modern {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 25px;
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .review-item-modern:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            border-color: rgba(179, 103, 255, 0.3);
        }

        .review-item-modern::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--neon-purple), var(--neon-pink));
        }

        .review-header {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .review-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 1.5rem;
            margin-right: 15px;
        }

        .review-author-info {
            flex: 1;
        }

        .review-author-name {
            font-size: 1.2rem;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .review-date {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .review-rating-stars {
            color: #ffd700;
            font-size: 1.2rem;
            margin-bottom: 15px;
        }

        .review-text-modern {
            font-size: 1rem;
            line-height: 1.6;
            color: var(--text-primary);
        }

        .review-quote {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 3rem;
            color: rgba(255, 255, 255, 0.1);
        }

        /* НОВЫЕ СТИЛИ ДЛЯ УЛУЧШЕННОГО ЛИЧНОГО КАБИНЕТА */
        .profile-card-modern {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 30px;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .profile-card-modern::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--neon-purple), var(--neon-pink));
        }

        .profile-avatar-modern {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 2.5rem;
            margin: 0 auto 20px;
            position: relative;
            overflow: hidden;
            border: 4px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .profile-avatar-modern:hover {
            transform: scale(1.05);
            border-color: rgba(179, 103, 255, 0.5);
        }

        .profile-avatar-modern img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .profile-info-modern {
            text-align: center;
            margin-bottom: 25px;
        }

        .profile-name-modern {
            font-size: 1.8rem;
            font-weight: bold;
            margin-bottom: 5px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .profile-email-modern {
            color: var(--text-secondary);
            font-size: 1rem;
            margin-bottom: 15px;
        }

        .profile-status-modern {
            display: inline-block;
            padding: 5px 15px;
            background: rgba(76, 175, 80, 0.2);
            color: #4caf50;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: bold;
        }

        .profile-stats-modern {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-bottom: 25px;
        }

        .profile-stat-item {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 15px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .profile-stat-item:hover {
            background: rgba(255, 255, 255, 0.08);
            transform: translateY(-3px);
        }

        .profile-stat-number {
            font-size: 1.8rem;
            font-weight: bold;
            margin-bottom: 5px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .profile-stat-label {
            font-size: 0.9rem;
            color: var(--text-secondary);
        }

        .profile-badges-modern {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 25px;
            flex-wrap: wrap;
        }

        .profile-badge-modern {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            color: white;
            border-radius: 20px;
            padding: 8px 15px;
            font-size: 0.8rem;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 5px;
            box-shadow: 0 4px 10px rgba(83, 52, 131, 0.3);
        }

        .profile-progress-modern {
            margin-bottom: 25px;
        }

        .profile-progress-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-size: 0.9rem;
        }

        .profile-progress-bar {
            height: 8px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            overflow: hidden;
        }

        .profile-progress-fill {
            height: 100%;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            border-radius: 4px;
            width: 65%;
        }

        .profile-actions-modern {
            display: flex;
            gap: 10px;
        }

        /* НОВЫЙ СТИЛЬ: АСИММЕТРИЧНЫЙ ПРОФИЛЬ */
        .asymmetric-profile {
            display: grid;
            grid-template-columns: 1fr 1.2fr;
            gap: 30px;
            margin-top: 30px;
        }

        .profile-main {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .profile-sidebar {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .profile-widget {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .profile-widget:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        .activity-map {
            height: 200px;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            border-radius: 15px;
            position: relative;
            overflow: hidden;
        }

        .activity-dots {
            position: absolute;
            width: 100%;
            height: 100%;
        }

        .activity-dot {
            position: absolute;
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.7);
            animation: pulse-dot 2s infinite;
        }

        @keyframes pulse-dot {
            0% { transform: scale(1); opacity: 0.7; }
            50% { transform: scale(1.5); opacity: 1; }
            100% { transform: scale(1); opacity: 0.7; }
        }

        .stat-visual {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-top: 15px;
        }

        .stat-bar {
            flex: 1;
            height: 8px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            margin: 0 10px;
            overflow: hidden;
        }

        .stat-fill {
            height: 100%;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            border-radius: 4px;
        }

        /* Анимация для звезд рейтинга */
        .rating-stars {
            font-size: 24px;
            margin: 10px 0;
        }
        
        .rating-star {
            cursor: pointer;
            margin: 0 2px;
            transition: all 0.3s ease;
        }
        
        .rating-star:hover {
            transform: scale(1.2);
            text-shadow: 0 0 10px rgba(255, 255, 0, 0.7);
        }
        
        .rating-star.active {
            color: #ffc107;
            text-shadow: 0 0 10px rgba(255, 193, 7, 0.7);
        }
        
        .chat-container {
            height: 500px;
            overflow-y: auto;
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            margin-bottom: 15px;
        }
        
        .chat-message {
            margin-bottom: 15px;
            padding: 10px 15px;
            border-radius: 15px;
            max-width: 80%;
            position: relative;
        }
        
        .chat-message.own {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            margin-left: auto;
            border-bottom-right-radius: 5px;
        }
        
        .chat-message.other {
            background: rgba(255, 255, 255, 0.1);
            border-bottom-left-radius: 5px;
        }
        
        .chat-message .sender {
            font-weight: bold;
            margin-bottom: 5px;
            font-size: 0.9rem;
        }
        
        .chat-message .time {
            font-size: 0.7rem;
            opacity: 0.7;
            text-align: right;
            margin-top: 5px;
        }
        
        .user-avatar {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            box-shadow: 0 4px 10px rgba(83, 52, 131, 0.4);
            font-size: 2rem;
            overflow: hidden;
        }
        
        .user-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .small-avatar {
            width: 40px;
            height: 40px;
            font-size: 1rem;
        }
        
        .notification {
            position: fixed;
            top: 100px;
            right: 20px;
            padding: 15px 25px;
            background: var(--accent);
            color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            z-index: 1000;
            transform: translateX(150%);
            transition: transform 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
        }
        
        .notification.show {
            transform: translateX(0);
        }
        
        .loader {
            display: inline-block;
            width: 30px;
            height: 30px;
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: var(--accent);
            animation: spin 1s ease-in-out infinite;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        .order-form {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .telegram-preview {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            max-width: 600px;
            margin: 0 auto;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease;
        }
        
        .telegram-preview:hover {
            transform: scale(1.03);
        }
        
        .telegram-header {
            background: #5682a3;
            color: white;
            padding: 12px 15px;
            display: flex;
            align-items: center;
        }
        
        .telegram-content {
            padding: 15px;
            color: #333;
        }
        
        .telegram-message {
            background: #e8f4f9;
            border-radius: 12px;
            padding: 10px 15px;
            margin-bottom: 10px;
            position: relative;
        }
        
        .telegram-message:after {
            content: '';
            position: absolute;
            left: -10px;
            top: 10px;
            width: 0;
            height: 0;
            border: 10px solid transparent;
            border-right-color: #e8f4f9;
        }
        
        .telegram-image {
            width: 100%;
            border-radius: 10px;
            margin: 10px 0;
        }
        
        .telegram-footer {
            padding: 10px 15px;
            border-top: 1px solid #eee;
            display: flex;
            justify-content: space-between;
        }
        
        .login-container {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, rgba(26, 26, 46, 0.9), rgba(22, 33, 62, 0.9));
            position: relative;
            overflow: hidden;
        }
        
        .login-container::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(179, 103, 255, 0.1) 0%, rgba(26, 26, 46, 0) 70%);
            animation: rotate 20s linear infinite;
        }
        
        @keyframes rotate {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }
        
        .login-card {
            width: 100%;
            max-width: 450px;
            z-index: 1;
        }
        
        .floating-icons {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 0;
        }
        
        .floating-icons i {
            position: absolute;
            color: rgba(179, 103, 255, 0.2);
            font-size: 24px;
            animation: float 6s ease-in-out infinite;
        }
        
        .floating-icons i:nth-child(1) {
            top: 10%;
            left: 10%;
            animation-delay: 0s;
        }
        
        .floating-icons i:nth-child(2) {
            top: 20%;
            right: 15%;
            animation-delay: 1s;
        }
        
        .floating-icons i:nth-child(3) {
            bottom: 30%;
            left: 15%;
            animation-delay: 2s;
        }
        
        .floating-icons i:nth-child(4) {
            bottom: 20%;
            right: 10%;
            animation-delay: 3s;
        }
        
        .floating-icons i:nth-child(5) {
            top: 50%;
            left: 5%;
            animation-delay: 4s;
        }

        /* Стили для анимированных переходов между разделами */
        .page-transition {
            animation: pageTransition 0.5s ease;
        }

        @keyframes pageTransition {
            0% { opacity: 0; transform: translateY(20px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        /* 3D эффект для аватара */
        .avatar-3d {
            transform-style: preserve-3d;
            transition: transform 0.5s ease;
        }

        .avatar-3d:hover {
            transform: rotateY(10deg) rotateX(5deg);
        }

        .admin-badge {
            background: linear-gradient(135deg, var(--neon-pink), var(--accent));
            color: white;
            padding: 3px 10px;
            border-radius: 20px;
            font-size: 0.7rem;
            font-weight: bold;
            margin-left: 5px;
        }
        
        .status-online {
            color: #4ade80;
        }
        
        .status-offline {
            color: #f87171;
        }
        
        .avatar-upload {
            position: relative;
            display: inline-block;
            cursor: pointer;
        }
        
        .avatar-upload input {
            display: none;
        }
        
        .avatar-edit {
            position: absolute;
            bottom: 0;
            right: 0;
            background: var(--accent);
            border-radius: 50%;
            width: 30px;
            height: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
        }
        
        .order-history {
            max-height: 400px;
            overflow-y: auto;
        }
        
        .order-item {
            border-left: 3px solid var(--purple);
            padding-left: 15px;
            margin-bottom: 15px;
        }

        /* Улучшенные стили для текста в полях ввода */
        input::placeholder, textarea::placeholder {
            color: var(--text-secondary) !important;
            opacity: 0.7;
        }

        input, textarea, select {
            color: var(--text-primary) !important;
        }

        /* КРИТИЧЕСКИЕ ИСПРАВЛЕНИЯ ДЛЯ ПРОБЛЕМ С ТЕКСТОМ */

        /* Исправление для первого скриншота - невидимого текста */
        .stars-text-section {
            color: var(--text-primary) !important;
            opacity: 1 !important;
            font-size: 1rem !important;
            position: static !important;
            visibility: visible !important;
        }

        /* Исправление для админ-панели - серого текста на темном фоне */
        .admin-table-container,
        .admin-widget,
        .admin-quick-action,
        .admin-stat-card {
            color: var(--text-primary) !important;
        }

        .admin-table-container th,
        .admin-table-container td {
            color: var(--text-primary) !important;
        }

        /* Исправление для выпадающих списков - невидимого текста по умолчанию */
        .form-select {
            color: var(--text-primary) !important;
            background-color: rgba(255, 255, 255, 0.1) !important;
            border: 1px solid rgba(255, 255, 255, 0.2) !important;
        }

        .form-select option {
            color: var(--text-primary) !important;
            background-color: var(--bg-secondary) !important;
        }

        /* Улучшение контраста для всех текстов */
        .text-muted {
            color: var(--text-secondary) !important;
        }

        /* Стили для загрузки аватара */
        .avatar-upload-area {
            border: 2px dashed var(--neon-purple);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-bottom: 15px;
        }

        .avatar-upload-area:hover {
            border-color: var(--neon-pink);
            background: rgba(179, 103, 255, 0.1);
        }

        .avatar-upload-icon {
            font-size: 3rem;
            color: var(--neon-purple);
            margin-bottom: 10px;
        }

        .avatar-preview {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--neon-purple);
            margin: 0 auto;
            display: none;
        }

        .avatar-upload-info {
            font-size: 0.9rem;
            color: var(--text-secondary);
            margin-top: 10px;
        }

        /* Улучшенные стили для мобильных устройств */
        @media (max-width: 576px) {
            .container {
                padding-left: 10px;
                padding-right: 10px;
            }
            
            .hero-section {
                padding: 80px 0 30px;
            }
            
            .display-4 {
                font-size: 1.8rem;
            }
            
            .hero-subtitle {
                font-size: 1rem;
            }
            
            .btn-lg {
                padding: 10px 20px;
                font-size: 0.9rem;
            }
            
            .glass-card {
                padding: 15px;
            }
            
            .profile-avatar-modern {
                width: 80px;
                height: 80px;
                font-size: 1.8rem;
            }
            
            .profile-name-modern {
                font-size: 1.4rem;
            }
            
            .admin-table-container {
                padding: 10px;
            }
            
            .admin-search-box {
                width: 100%;
                margin-bottom: 10px;
            }
            
            .admin-table-header {
                flex-direction: column;
                gap: 10px;
            }
            
            .navbar-brand {
                font-size: 1rem;
            }
            
            .chat-container {
                height: 300px;
                padding: 15px;
            }
            
            .stars-visual .star-visual {
                font-size: 2rem;
            }
        }

        /* НОВЫЕ СТИЛИ ДЛЯ УЛУЧШЕННОЙ СТРАНИЦЫ ЗВЕЗД */
        .stars-hero-section {
            min-height: 60vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, rgba(26, 26, 46, 0.9), rgba(22, 33, 62, 0.9));
            position: relative;
            overflow: hidden;
        }
        
        .stars-animation-container {
            position: relative;
            width: 100%;
            height: 300px;
            margin: 40px 0;
        }
        
        .stars-animation {
            position: absolute;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, rgba(255, 215, 0, 0.2) 0%, transparent 70%);
            animation: stars-pulse 3s infinite alternate;
        }
        
        @keyframes stars-pulse {
            0% { transform: scale(1); opacity: 0.5; }
            100% { transform: scale(1.1); opacity: 1; }
        }
        
        .floating-star {
            position: absolute;
            color: #ffd700;
            font-size: 2rem;
            animation: float-star 6s infinite ease-in-out;
        }
        
        @keyframes float-star {
            0% { transform: translate(0, 0) rotate(0deg); opacity: 0.7; }
            50% { transform: translate(20px, -20px) rotate(180deg); opacity: 1; }
            100% { transform: translate(0, 0) rotate(360deg); opacity: 0.7; }
        }
        
        .premium-badge {
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            color: #333;
            border-radius: 20px;
            padding: 8px 15px;
            font-weight: bold;
            display: inline-block;
            margin: 10px 0;
            box-shadow: 0 4px 10px rgba(255, 215, 0, 0.3);
        }
        
        .stars-feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }
        
        .stars-feature-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .stars-feature-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .stars-feature-icon {
            font-size: 3rem;
            margin-bottom: 15px;
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .stars-pricing-table {
            width: 100%;
            border-collapse: collapse;
            margin: 30px 0;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            overflow: hidden;
        }
        
        .stars-pricing-table th,
        .stars-pricing-table td {
            padding: 15px;
            text-align: center;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .stars-pricing-table th {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            color: white;
            font-weight: bold;
        }
        
        .stars-pricing-table tr:last-child td {
            border-bottom: none;
        }
        
        .stars-pricing-table tr:hover {
            background: rgba(255, 255, 255, 0.05);
        }
        
        .stars-benefits-list {
            list-style: none;
            padding: 0;
            margin: 20px 0;
        }
        
        .stars-benefits-list li {
            padding: 10px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
        }
        
        .stars-benefits-list li:last-child {
            border-bottom: none;
        }
        
        .stars-benefits-list li::before {
            content: '✓';
            color: #ffd700;
            margin-right: 10px;
            font-weight: bold;
            font-size: 1.2rem;
        }

        /* НОВЫЙ СТИЛЬ ДЛЯ СТРАНИЦЫ ЗВЕЗД И PREMIUM */
        .stars-premium-hero {
            min-height: 70vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            background: linear-gradient(135deg, rgba(26, 26, 46, 0.9), rgba(22, 33, 62, 0.9));
        }
        
        .stars-premium-animation {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        
        .floating-premium-icon {
            position: absolute;
            font-size: 3rem;
            color: rgba(255, 215, 0, 0.3);
            animation: float-premium 8s infinite ease-in-out;
        }
        
        @keyframes float-premium {
            0% { transform: translate(0, 0) rotate(0deg) scale(1); }
            25% { transform: translate(50px, -30px) rotate(90deg) scale(1.2); }
            50% { transform: translate(0, -50px) rotate(180deg) scale(1); }
            75% { transform: translate(-50px, -30px) rotate(270deg) scale(1.2); }
            100% { transform: translate(0, 0) rotate(360deg) scale(1); }
        }
        
        .premium-feature-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        .premium-feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #ffd700, #ffed4e);
        }
        
        .premium-feature-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }
        
        .premium-feature-icon {
            font-size: 4rem;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .premium-guarantee {
            background: linear-gradient(135deg, rgba(255, 215, 0, 0.1), rgba(255, 237, 78, 0.1));
            border: 1px solid rgba(255, 215, 0, 0.3);
            border-radius: 15px;
            padding: 20px;
            margin: 30px 0;
        }
        
        .premium-stats {
            display: flex;
            justify-content: space-around;
            margin: 40px 0;
            text-align: center;
        }
        
        .premium-stat {
            padding: 20px;
        }
        
        .premium-stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }
        
        .premium-stat-label {
            font-size: 1.1rem;
            opacity: 0.8;
        }

        /* НОВЫЙ СТИЛЬ ДЛЯ GALAXY STARS & PREMIUM */
        .galaxy-hero {
            min-height: 80vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            background: linear-gradient(135deg, #0c0c1f, #1a1a3e, #2d2d5a);
        }
        
        .galaxy-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 30%, rgba(179, 103, 255, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 70%, rgba(255, 42, 109, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 80%, rgba(255, 215, 0, 0.1) 0%, transparent 50%);
            animation: galaxy-pulse 10s infinite alternate;
        }
        
        @keyframes galaxy-pulse {
            0% { opacity: 0.5; }
            100% { opacity: 1; }
        }
        
        .galaxy-stars {
            position: absolute;
            width: 100%;
            height: 100%;
        }
        
        .galaxy-star {
            position: absolute;
            background: white;
            border-radius: 50%;
            animation: twinkle 3s infinite alternate;
        }
        
        .galaxy-star:nth-child(1) { top: 10%; left: 15%; width: 3px; height: 3px; animation-delay: 0s; }
        .galaxy-star:nth-child(2) { top: 20%; left: 80%; width: 2px; height: 2px; animation-delay: 0.5s; }
        .galaxy-star:nth-child(3) { top: 60%; left: 10%; width: 4px; height: 4px; animation-delay: 1s; }
        .galaxy-star:nth-child(4) { top: 80%; left: 70%; width: 2px; height: 2px; animation-delay: 1.5s; }
        .galaxy-star:nth-child(5) { top: 40%; left: 90%; width: 3px; height: 3px; animation-delay: 2s; }
        
        .galaxy-title {
            font-size: 4rem;
            font-weight: bold;
            background: linear-gradient(135deg, #ffd700, #ffed4e, #b967ff, #ff2a6d);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-align: center;
            margin-bottom: 1rem;
            text-shadow: 0 0 30px rgba(255, 215, 0, 0.5);
        }
        
        .galaxy-subtitle {
            font-size: 1.5rem;
            text-align: center;
            margin-bottom: 2rem;
            color: var(--text-secondary);
        }
        
        .galaxy-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        
        .galaxy-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #ffd700, #ffed4e, #b967ff, #ff2a6d);
        }
        
        .galaxy-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }
        
        .galaxy-icon {
            font-size: 4rem;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .galaxy-badge {
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            color: #333;
            border-radius: 20px;
            padding: 8px 15px;
            font-weight: bold;
            display: inline-block;
            margin: 10px 0;
            box-shadow: 0 4px 10px rgba(255, 215, 0, 0.3);
        }
        
        .galaxy-btn {
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            color: #333;
            border: none;
            border-radius: 12px;
            padding: 15px 30px;
            font-weight: bold;
            font-size: 1.2rem;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(255, 215, 0, 0.4);
            display: block;
            width: 100%;
            text-align: center;
            margin-top: 20px;
        }
        
        .galaxy-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 215, 0, 0.6);
            color: #333;
        }
        
        .galaxy-steps {
            display: flex;
            flex-direction: column;
            gap: 20px;
            margin: 40px 0;
        }
        
        .galaxy-step {
            display: flex;
            align-items: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            transition: all 0.3s ease;
        }
        
        .galaxy-step:hover {
            background: rgba(255, 255, 255, 0.08);
            transform: translateX(10px);
        }
        
        .galaxy-step-number {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, #ffd700, #ffed4e);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.5rem;
            margin-right: 20px;
            flex-shrink: 0;
            color: #333;
        }
        
        .galaxy-step-content {
            flex: 1;
        }
        
        .galaxy-step-title {
            font-size: 1.3rem;
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .galaxy-step-description {
            color: var(--text-secondary);
        }

        /* Стили для карусели отзывов */
        .reviews-carousel {
            position: relative;
            padding: 20px 0;
        }
        
        .reviews-carousel-inner {
            display: flex;
            overflow-x: auto;
            gap: 20px;
            padding: 20px 0;
            scroll-behavior: smooth;
            scrollbar-width: none; /* Firefox */
        }
        
        .reviews-carousel-inner::-webkit-scrollbar {
            display: none; /* Chrome, Safari, Edge */
        }
        
        .review-carousel-item {
            flex: 0 0 auto;
            width: 350px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 25px;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .review-carousel-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            border-color: rgba(179, 103, 255, 0.3);
        }
        
        .carousel-controls {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
        }
        
        .carousel-control {
            background: rgba(255, 255, 255, 0.1);
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .carousel-control:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: scale(1.1);
        }

        /* НОВЫЕ СТИЛИ ДЛЯ ЦЕНТРИРОВАННОЙ ЗАГРУЗКИ АВАТАРА */
        .avatar-upload-center {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin: 20px 0;
        }

        .avatar-preview-container {
            position: relative;
            width: 150px;
            height: 150px;
            margin-bottom: 20px;
        }

        .avatar-preview-center {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--neon-purple);
            box-shadow: 0 0 20px rgba(179, 103, 255, 0.5);
        }

        .avatar-upload-center .avatar-edit {
            position: absolute;
            bottom: -20px;
            right: 5px;
            background: var(--accent);
            border-radius: 50%;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 2px 10px rgba(233, 69, 96, 0.4);
        }

        .avatar-upload-center .avatar-edit:hover {
            transform: scale(1.1);
        }

        /* НОВЫЕ СТИЛИ ДЛЯ УЛУЧШЕННОЙ СТРАНИЦЫ "О НАС" */
        .about-hero-modern {
            min-height: 70vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            background: linear-gradient(135deg, rgba(26, 26, 46, 0.9), rgba(22, 33, 62, 0.9));
        }

        .about-hero-modern::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 30% 20%, rgba(179, 103, 255, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 70% 80%, rgba(255, 42, 109, 0.1) 0%, transparent 50%);
            z-index: -1;
        }

        .about-telegram-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 50px 0;
        }

        .telegram-card-modern {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            overflow: hidden;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .telegram-card-modern:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            border-color: rgba(179, 103, 255, 0.3);
        }

        .telegram-card-header {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            padding: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .telegram-card-icon {
            font-size: 2rem;
        }

        .telegram-card-content {
            padding: 25px;
        }

        .telegram-card-description {
            margin-bottom: 20px;
            color: var(--text-secondary);
        }

        .contact-admin-modern {
            background: linear-gradient(135deg, rgba(179, 103, 255, 0.1), rgba(255, 42, 109, 0.1));
            border-radius: 20px;
            padding: 40px;
            margin-top: 50px;
            text-align: center;
            border: 1px solid rgba(179, 103, 255, 0.2);
        }

        .contact-admin-modern h3 {
            margin-bottom: 20px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* НОВЫЙ СТИЛЬ ДЛЯ УЛУЧШЕННОГО ЛИЧНОГО КАБИНЕТА */
        .new-dashboard {
            padding: 30px 0;
        }

        .dashboard-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 30px;
        }

        .dashboard-welcome {
            font-size: 2.5rem;
            font-weight: bold;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .dashboard-stats-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .dashboard-stat-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 25px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .dashboard-stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--neon-purple), var(--neon-pink));
        }

        .dashboard-stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }

        .dashboard-stat-icon {
            font-size: 3rem;
            margin-bottom: 15px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .dashboard-stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .dashboard-stat-label {
            font-size: 1rem;
            color: var(--text-secondary);
        }

        .dashboard-content {
            display: grid;
            grid-template-columns: 1fr 1.2fr;
            gap: 30px;
        }

        .profile-section {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .profile-avatar-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 30px;
        }

        .profile-avatar-large {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 3rem;
            margin-bottom: 20px;
            position: relative;
            overflow: hidden;
            border: 4px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .profile-avatar-large:hover {
            transform: scale(1.05);
            border-color: rgba(179, 103, 255, 0.5);
        }

        .profile-avatar-large img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .avatar-upload-btn {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            color: white;
            border: none;
            border-radius: 10px;
            padding: 10px 20px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .avatar-upload-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(83, 52, 131, 0.4);
        }

        .profile-info-section {
            margin-bottom: 30px;
        }

        .profile-name {
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 10px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .profile-email {
            font-size: 1.2rem;
            color: var(--text-secondary);
            margin-bottom: 20px;
        }

        .profile-badges-section {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-bottom: 30px;
        }

        .profile-badge-new {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            color: white;
            border-radius: 20px;
            padding: 8px 15px;
            font-size: 0.8rem;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .profile-actions-section {
            display: flex;
            gap: 10px;
        }

        .profile-action-btn {
            flex: 1;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: var(--text-primary);
            border-radius: 10px;
            padding: 12px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .profile-action-btn:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-3px);
        }

        .orders-section {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .orders-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }

        .orders-title {
            font-size: 1.8rem;
            font-weight: bold;
        }

        .orders-filter {
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            padding: 8px 15px;
            color: var(--text-primary);
        }

        .orders-list {
            max-height: 500px;
            overflow-y: auto;
        }

        .order-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            margin-bottom: 15px;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .order-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .order-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .order-title {
            font-size: 1.3rem;
            font-weight: bold;
        }

        .order-status {
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
        }

        .order-status.completed {
            background: rgba(76, 175, 80, 0.2);
            color: #4caf50;
        }

        .order-status.pending {
            background: rgba(255, 193, 7, 0.2);
            color: #ffc107;
        }

        .order-details {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-bottom: 15px;
        }

        .order-detail {
            display: flex;
            justify-content: space-between;
        }

        .order-detail-label {
            color: var(--text-secondary);
        }

        .order-actions {
            display: flex;
            gap: 10px;
        }

        .order-action-btn {
            flex: 1;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: var(--text-primary);
            border-radius: 8px;
            padding: 8px;
            text-align: center;
            transition: all 0.3s ease;
            font-size: 0.9rem;
        }

        .order-action-btn:hover {
            background: rgba(255, 255, 255, 0.2);
        }

        .order-action-btn.review {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            color: white;
        }

        .order-action-btn.review:hover {
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
        }

        /* Стили для модального окна загрузки аватара */
        .avatar-modal .modal-content {
            background: var(--bg-secondary);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .avatar-modal .modal-header {
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .avatar-modal .modal-body {
            padding: 30px;
        }

        .avatar-preview-modal {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            margin: 0 auto 20px;
            background: rgba(255, 255, 255, 0.05);
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            border: 3px solid var(--neon-purple);
        }

        .avatar-preview-modal img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .avatar-upload-zone {
            border: 2px dashed var(--neon-purple);
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-bottom: 20px;
        }

        .avatar-upload-zone:hover {
            border-color: var(--neon-pink);
            background: rgba(179, 103, 255, 0.1);
        }

        .avatar-upload-icon {
            font-size: 3rem;
            color: var(--neon-purple);
            margin-bottom: 15px;
        }

        .avatar-upload-text {
            font-size: 1.1rem;
            margin-bottom: 10px;
        }

        .avatar-upload-info {
            font-size: 0.9rem;
            color: var(--text-secondary);
        }

        .avatar-crop-container {
            width: 100%;
            height: 300px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 20px;
        }

        .avatar-crop-controls {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }

        .avatar-crop-btn {
            flex: 1;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: var(--text-primary);
            border-radius: 8px;
            padding: 10px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .avatar-crop-btn:hover {
            background: rgba(255, 255, 255, 0.2);
        }

        .avatar-crop-btn.apply {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            color: white;
        }

        .avatar-crop-btn.apply:hover {
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
        }

        /* НОВЫЕ СТИЛИ ДЛЯ ФОРМ АВТОРИЗАЦИИ */
        .auth-form-container {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, rgba(26, 26, 46, 0.9), rgba(22, 33, 62, 0.9));
            position: relative;
            overflow: hidden;
        }

        .auth-form-container::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(179, 103, 255, 0.1) 0%, rgba(26, 26, 46, 0) 70%);
            animation: rotate 20s linear infinite;
        }

        .auth-card {
            width: 100%;
            max-width: 450px;
            z-index: 1;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(15px);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }

        .auth-header {
            padding: 30px 30px 20px;
            text-align: center;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .auth-title {
            font-size: 2rem;
            font-weight: bold;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }

        .auth-subtitle {
            color: var(--text-secondary);
            font-size: 1rem;
        }

        .auth-body {
            padding: 30px;
        }

        .form-group {
            margin-bottom: 20px;
            position: relative;
        }

        .form-input {
            width: 100%;
            padding: 15px 20px;
            background: rgba(255, 255, 255, 0.08);
            border: 2px solid transparent;
            border-radius: 12px;
            color: var(--text-primary);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-input:focus {
            outline: none;
            border-color: var(--neon-purple);
            box-shadow: 0 0 0 3px rgba(179, 103, 255, 0.2);
            background: rgba(255, 255, 255, 0.12);
        }

        .form-input::placeholder {
            color: var(--text-secondary);
        }

        .form-label {
            position: absolute;
            left: 20px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--text-secondary);
            transition: all 0.3s ease;
            pointer-events: none;
            background: var(--bg-secondary);
            padding: 0 8px;
        }

        .form-input:focus + .form-label,
        .form-input:not(:placeholder-shown) + .form-label {
            top: 0;
            font-size: 0.8rem;
            color: var(--neon-purple);
        }

        .captcha-container {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 20px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .captcha-text {
            font-size: 1.8rem;
            font-weight: bold;
            letter-spacing: 5px;
            color: var(--text-primary);
            margin-bottom: 15px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: blur(0.5px);
            transform: skew(-5deg);
        }

        .captcha-input {
            width: 100%;
            padding: 12px 15px;
            background: rgba(255, 255, 255, 0.08);
            border: 2px solid transparent;
            border-radius: 8px;
            color: var(--text-primary);
            text-align: center;
            font-size: 1.1rem;
            letter-spacing: 2px;
            transition: all 0.3s ease;
        }

        .captcha-input:focus {
            outline: none;
            border-color: var(--neon-cyan);
            box-shadow: 0 0 0 3px rgba(0, 243, 255, 0.2);
        }

        .auth-footer {
            padding: 0 30px 30px;
            text-align: center;
        }

        .auth-link {
            color: var(--neon-purple);
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .auth-link:hover {
            color: var(--neon-pink);
            text-decoration: underline;
        }

        /* Стили для частиц */
        #particles-js {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 0;
        }

        /* НОВЫЕ СТИЛИ ДЛЯ AI-ЧАТА */
        .ai-chat-container {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }

        .ai-chat-header {
            background: linear-gradient(135deg, var(--purple), var(--neon-purple));
            padding: 20px;
            text-align: center;
        }

        .ai-chat-title {
            font-size: 1.5rem;
            font-weight: bold;
            margin: 0;
        }

        .ai-chat-body {
            height: 400px;
            overflow-y: auto;
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .ai-message {
            max-width: 80%;
            padding: 15px 20px;
            border-radius: 20px;
            position: relative;
            animation: messageSlide 0.3s ease;
        }

        @keyframes messageSlide {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .ai-message.user {
            align-self: flex-end;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            border-bottom-right-radius: 5px;
        }

        .ai-message.bot {
            align-self: flex-start;
            background: rgba(255, 255, 255, 0.1);
            border-bottom-left-radius: 5px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .ai-typing {
            display: flex;
            align-items: center;
            gap: 5px;
            padding: 10px 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            align-self: flex-start;
            max-width: 80px;
        }

        .typing-dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background: var(--neon-purple);
            animation: typingAnimation 1.4s infinite ease-in-out;
        }

        .typing-dot:nth-child(1) { animation-delay: -0.32s; }
        .typing-dot:nth-child(2) { animation-delay: -0.16s; }

        @keyframes typingAnimation {
            0%, 80%, 100% {
                transform: scale(0.8);
                opacity: 0.5;
            }
            40% {
                transform: scale(1);
                opacity: 1;
            }
        }

        .ai-quick-replies {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            padding: 15px 20px;
            background: rgba(255, 255, 255, 0.03);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .quick-reply-btn {
            padding: 8px 16px;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            color: var(--text-primary);
            font-size: 0.9rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .quick-reply-btn:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-2px);
        }

        .ai-chat-input {
            display: flex;
            padding: 20px;
            gap: 10px;
            background: rgba(255, 255, 255, 0.03);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .chat-input {
            flex: 1;
            padding: 12px 20px;
            background: rgba(255, 255, 255, 0.08);
            border: 2px solid transparent;
            border-radius: 25px;
            color: var(--text-primary);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .chat-input:focus {
            outline: none;
            border-color: var(--neon-purple);
            background: rgba(255, 255, 255, 0.12);
        }

        .send-btn {
            padding: 12px 25px;
            background: linear-gradient(135deg, var(--neon-purple), var(--neon-pink));
            border: none;
            border-radius: 25px;
            color: white;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .send-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(179, 103, 255, 0.4);
        }

        /* Стили для кнопки Galaxy Stars */
        .galaxy-stars-btn {
            background: linear-gradient(135deg, #ffd700, #ffed4e, #b967ff, #ff2a6d);
            color: #333;
            border: none;
            border-radius: 25px;
            padding: 15px 30px;
            font-weight: bold;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(255, 215, 0, 0.4);
            position: relative;
            overflow: hidden;
            animation: pulse 2s infinite;
        }

        .galaxy-stars-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 215, 0, 0.6);
            animation: none;
        }

        .galaxy-stars-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.5s ease;
        }

        .galaxy-stars-btn:hover::before {
            left: 100%;
        }

        /* Стили для sticky кнопки */
        .sticky-galaxy-btn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 1000;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-10px);
            }
            60% {
                transform: translateY(-5px);
            }
        }

        /* Стили для выделения секции */
        .highlight-section {
            animation: highlight 2s ease;
            box-shadow: 0 0 30px rgba(255, 215, 0, 0.5);
        }

        @keyframes highlight {
            0% {
                box-shadow: 0 0 0 0 rgba(255, 215, 0, 0.5);
            }
            50% {
                box-shadow: 0 0 30px 10px rgba(255, 215, 0, 0.5);
            }
            100% {
                box-shadow: 0 0 30px rgba(255, 215, 0, 0.5);
            }
        }
    </style>
</head>
<body>
    <!-- Анимированный фон -->
    <div class="bg-animation">
        <div class="ball ball-1"></div>
        <div class="ball ball-2"></div>
        <div class="ball ball-3"></div>
    </div>
    
    <!-- Навигационное меню -->
    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#" data-page="home">
                <i class="fas fa-star me-2"></i>st1xlox Services
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item">
                        <a class="nav-link active" href="#" data-page="home">Главная</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" data-page="orders">Оформление заказа</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" data-page="stars">Galaxy Stars&Premium</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" data-page="about">О нас</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" data-page="reviews">Отзывы</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" data-page="chat">st1xlox AI-Chat</a>
                    </li>
                </ul>
                <ul class="navbar-nav" id="auth-nav">
                    <li class="nav-item">
                        <a class="nav-link" href="#" data-page="login">Войти</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" data-page="register">Регистрация</a>
                    </li>
                </ul>
                <ul class="navbar-nav d-none" id="user-nav">
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown">
                            <div class="user-avatar small-avatar me-2" id="user-avatar">U</div>
                            <span id="username-display">Пользователь</span>
                            <span class="admin-badge d-none" id="admin-badge">ADMIN</span>
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="#" data-page="dashboard">Личный кабинет</a></li>
                            <li><a class="dropdown-item d-none admin-only" href="#" data-page="admin">Админ панель</a></li>
                            <li><hr class="dropdown-divider"></li>
                            <li><a class="dropdown-item" href="#" id="logout-btn">Выйти</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Система уведомлений -->
    <div class="notification-system" id="notification-system"></div>

    <!-- Модальное окно для отзывов о заказах -->
    <div class="modal fade" id="orderReviewModal" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content glass-card">
                <div class="modal-header">
                    <h5 class="modal-title">Оставить отзыв о заказе</h5>
                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="order-review-form">
                        <input type="hidden" id="review-order-id">
                        <div class="mb-3">
                            <label for="review-order-text" class="form-label">Ваш отзыв</label>
                            <textarea class="form-control" id="review-order-text" rows="4" required></textarea>
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Оценка</label>
                            <div class="star-rating" id="order-rating-stars">
                                <span class="star" data-rating="1">★</span>
                                <span class="star" data-rating="2">★</span>
                                <span class="star" data-rating="3">★</span>
                                <span class="star" data-rating="4">★</span>
                                <span class="star" data-rating="5">★</span>
                            </div>
                            <input type="hidden" id="review-order-rating" value="0">
                        </div>
                        <button type="submit" class="btn btn-primary w-100">Отправить отзыв</button>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <!-- Модальное окно для загрузки аватара -->
    <div class="modal fade avatar-modal" id="avatarUploadModal" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title">Загрузка аватара</h5>
                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <div class="avatar-preview-modal" id="avatar-preview-modal">
                        <i class="fas fa-user" style="font-size: 4rem; color: rgba(255,255,255,0.5);"></i>
                    </div>
                    <div class="avatar-upload-zone" id="avatar-upload-zone">
                        <div class="avatar-upload-icon">
                            <i class="fas fa-cloud-upload-alt"></i>
                        </div>
                        <div class="avatar-upload-text">Перетащите изображение сюда или нажмите для выбора</div>
                        <div class="avatar-upload-info">Поддерживаются: JPG, PNG, GIF (макс. 5MB)</div>
                    </div>
                    <input type="file" id="avatar-file-input" accept=".jpg,.jpeg,.png,.gif" style="display: none;">
                    <div class="avatar-crop-controls d-none" id="avatar-crop-controls">
                        <button type="button" class="avatar-crop-btn" id="avatar-rotate-btn">
                            <i class="fas fa-redo"></i> Повернуть
                        </button>
                        <button type="button" class="avatar-crop-btn" id="avatar-zoom-in-btn">
                            <i class="fas fa-search-plus"></i> Увеличить
                        </button>
                        <button type="button" class="avatar-crop-btn" id="avatar-zoom-out-btn">
                            <i class="fas fa-search-minus"></i> Уменьшить
                        </button>
                    </div>
                    <div class="d-flex gap-2 mt-3">
                        <button type="button" class="btn btn-secondary w-50" data-bs-dismiss="modal">Отмена</button>
                        <button type="button" class="btn btn-primary w-50" id="avatar-save-btn">Сохранить</button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- УЛУЧШЕННАЯ ГЛАВНАЯ СТРАНИЦА -->
    <div id="home" class="page active-page page-transition">
        <section class="hero-section">
            <div class="hero-bg"></div>
            <div class="container hero-content">
                <div class="row align-items-center">
                    <div class="col-lg-6">
                        <h1 class="display-4 fw-bold mb-4 hero-animated-text">Премиальные услуги для вашего успеха</h1>
                        <p class="hero-subtitle">Мы создаем уникальные решения для продвижения вашего бренда в цифровом пространстве</p>
                        <div class="hero-cta-buttons">
                            <button class="btn btn-primary btn-lg pulse" data-page="orders">Сделать заказ</button>
                            <button class="btn btn-accent btn-lg" id="start-now-btn">Начать сейчас</button>
                            <button class="btn btn-outline-light btn-lg" data-page="chat">AI Помощник</button>
                        </div>
                    </div>
                    <div class="col-lg-6 text-center">
                        <div class="glass-card p-4 mt-5 mt-lg-0 floating-element">
                            <i class="fas fa-rocket display-1 text-accent mb-3"></i>
                            <h3>Инновационный подход</h3>
                            <p>Используем передовые технологии для достижения максимальных результатов</p>
                            <div class="mt-3">
                                <span class="badge bg-primary me-2">AI</span>
                                <span class="badge bg-success me-2">Инновации</span>
                                <span class="badge bg-warning">Качество</span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="hero-feature-grid">
                    <div class="hero-feature-card" data-service="video">
                        <div class="hero-feature-icon">
                            <i class="fas fa-video"></i>
                        </div>
                        <h4>Создание видео</h4>
                        <p>Профессиональные промо-ролики, интро и футажи для вашего бренда</p>
                        <div class="mt-3">
                            <span class="badge bg-primary">от 350 ₽</span>
                        </div>
                    </div>
                    <div class="hero-feature-card" data-service="design">
                        <div class="hero-feature-icon">
                            <i class="fas fa-palette"></i>
                        </div>
                        <h4>Графический дизайн</h4>
                        <p>Уникальные баннеры, посты для соцсетей и пикчи</p>
                        <div class="mt-3">
                            <span class="badge bg-primary">от 100 ₽</span>
                        </div>
                    </div>
                    <div class="hero-feature-card" data-service="avatar">
                        <div class="hero-feature-icon">
                            <i class="fas fa-user-circle"></i>
                        </div>
                        <h4>Дизайн аватарки</h4>
                        <p>Индивидуальные аватарки в аниме, фильм или собственном стиле</p>
                        <div class="mt-3">
                            <span class="badge bg-primary">от 100 ₽</span>
                        </div>
                    </div>
                    <div class="hero-feature-card" data-service="ads">
                        <div class="hero-feature-icon">
                            <i class="fas fa-ad"></i>
                        </div>
                        <h4>Рекламный пост</h4>
                        <p>Эффективное продвижение вашего проекта в Telegram</p>
                        <div class="mt-3">
                            <span class="badge bg-primary">от 350 ₽</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="py-5">
            <div class="container">
                <h2 class="text-center mb-5">Наши преимущества</h2>
                <div class="row g-4">
                    <div class="col-md-4">
                        <div class="glass-card p-4 text-center h-100">
                            <div class="feature-card-icon">
                                <i class="fas fa-lightbulb"></i>
                            </div>
                            <h4>Инновации</h4>
                            <p>Используем передовые технологии и методы для достижения выдающихся результатов</p>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="glass-card p-4 text-center h-100">
                            <div class="feature-card-icon">
                                <i class="fas fa-gem"></i>
                            </div>
                            <h4>Качество</h4>
                            <p>Гарантируем высочайшее качество всех предоставляемых услуг и решений</p>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="glass-card p-4 text-center h-100">
                            <div class="feature-card-icon">
                                <i class="fas fa-handshake"></i>
                            </div>
                            <h4>Надежность</h4>
                            <p>Строим долгосрочные отношения с клиентами, основанные на доверии и взаимовыгодном сотрудничестве</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- НОВАЯ СТРАНИЦА ЗАКАЗОВ С ИНТЕРАКТИВНЫМ КОНСТРУКТОРОМ -->
    <div id="orders" class="page page-transition">
        <div class="container py-5">
            <h1 class="text-center mb-5">Конструктор заказов</h1>

            <div class="order-constructor">
                <!-- Шаги конструктора -->
                <div class="constructor-steps">
                    <div class="step-indicator active" data-step="1">
                        <div class="step-circle">1</div>
                        <div>Выбор услуги</div>
                    </div>
                    <div class="step-indicator" data-step="2">
                        <div class="step-circle">2</div>
                        <div>Настройка</div>
                    </div>
                    <div class="step-indicator" data-step="3">
                        <div class="step-circle">3</div>
                        <div>Детали</div>
                    </div>
                    <div class="step-indicator" data-step="4">
                        <div class="step-circle">4</div>
                        <div>Подтверждение</div>
                    </div>
                </div>

                <div class="row">
                    <div class="col-lg-8">
                        <!-- Шаг 1: Выбор услуги -->
                        <div class="step-content active" data-step="1">
                            <div class="glass-card p-4 mb-4">
                                <h3 class="mb-4">Выберите тип услуги</h3>
                                <div class="service-options-grid">
                                    <div class="service-option-card active" data-service="video" data-base-price="350">
                                        <div class="service-icon">
                                            <i class="fas fa-video"></i>
                                        </div>
                                        <h5>Создание видео</h5>
                                        <p class="service-price">от 350 ₽</p>
                                        <ul class="option-features">
                                            <li data-price="500">Промо-ролик: 500 ₽</li>
                                            <li data-price="350">Интро/Аутро: 350 ₽</li>
                                            <li data-price="500">Футажи: 500 ₽</li>
                                        </ul>
                                    </div>
                                    <div class="service-option-card" data-service="images" data-base-price="100">
                                        <div class="service-icon">
                                            <i class="fas fa-image"></i>
                                        </div>
                                        <h5>Графический дизайн</h5>
                                        <p class="service-price">от 100 ₽</p>
                                        <ul class="option-features">
                                            <li data-price="200">Баннер: 200 ₽</li>
                                            <li data-price="100">Пост для соц. сетей: 100 ₽</li>
                                            <li data-price="150">Пикчи: 150 ₽</li>
                                        </ul>
                                    </div>
                                    <div class="service-option-card" data-service="avatar" data-base-price="100">
                                        <div class="service-icon">
                                            <i class="fas fa-user-circle"></i>
                                        </div>
                                        <h5>Дизайн аватарки</h5>
                                        <p class="service-price">от 100 ₽</p>
                                        <ul class="option-features">
                                            <li data-price="100">Аниме: 100 ₽</li>
                                            <li data-price="150">Фильм: 150 ₽</li>
                                            <li data-price="250">Сложная работа: 250 ₽</li>
                                        </ul>
                                    </div>
                                    <div class="service-option-card" data-service="ads" data-base-price="350">
                                        <div class="service-icon">
                                            <i class="fas fa-ad"></i>
                                        </div>
                                        <h5>Реклама в Telegram</h5>
                                        <p class="service-price">от 350 ₽</p>
                                        <ul class="option-features">
                                            <li data-price="350">1 день: 350 ₽</li>
                                            <li data-price="600">3 дня: 600 ₽</li>
                                            <li data-price="1200">7 дней: 1200 ₽</li>
                                            <li data-price="2000">14 дней: 2000 ₽</li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                            <div class="constructor-navigation">
                                <div></div> <!-- Пустой div для выравнивания -->
                                <button class="btn btn-primary next-step" data-next="2">Далее</button>
                            </div>
                        </div>

                        <!-- Шаг 2: Настройка услуги -->
                        <div class="step-content" data-step="2">
                            <div class="glass-card p-4 mb-4">
                                <h3 class="mb-4">Настройте вашу услугу</h3>
                                <div class="service-visual-preview">
                                    <div class="preview-animation"></div>
                                </div>
                                <div class="customization-options">
                                    <div class="customization-card">
                                        <h5>Стиль оформления</h5>
                                        <div class="form-check mt-3">
                                            <input class="form-check-input" type="radio" name="style" id="style-modern" checked>
                                            <label class="form-check-label" for="style-modern">
                                                Современный
                                            </label>
                                        </div>
                                        <div class="form-check">
                                            <input class="form-check-input" type="radio" name="style" id="style-minimal">
                                            <label class="form-check-label" for="style-minimal">
                                                Минимализм
                                            </label>
                                        </div>
                                        <div class="form-check">
                                            <input class="form-check-input" type="radio" name="style" id="style-luxury">
                                            <label class="form-check-label" for="style-luxury">
                                                Премиум
                                            </label>
                                        </div>
                                    </div>
                                    <div class="customization-card">
                                        <h5>Дополнительные опции</h5>
                                        <div class="form-check mt-3">
                                            <input class="form-check-input" type="checkbox" id="option-fast" data-multiplier="1.3">
                                            <label class="form-check-label" for="option-fast">
                                                Срочный заказ (+30%)
                                            </label>
                                        </div>
                                        <div class="form-check">
                                            <input class="form-check-input" type="checkbox" id="option-revisions">
                                            <label class="form-check-label" for="option-revisions">
                                                Дополнительные правки
                                            </label>
                                        </div>
                                        <div class="form-check">
                                            <input class="form-check-input" type="checkbox" id="option-support" data-add-price="100">
                                            <label class="form-check-label" for="option-support">
                                                Приоритетная поддержка (+100 ₽)
                                            </label>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="constructor-navigation">
                                <button class="btn btn-outline-primary prev-step" data-prev="1">Назад</button>
                                <button class="btn btn-primary next-step" data-next="3">Далее</button>
                            </div>
                        </div>

                        <!-- Шаг 3: Детали заказа -->
                        <div class="step-content" data-step="3">
                            <div class="glass-card p-4 mb-4">
                                <h3 class="mb-4">Детали заказа</h3>
                                <form id="order-details-form">
                                    <!-- Динамическое содержимое будет загружено здесь -->
                                </form>
                            </div>
                            <div class="constructor-navigation">
                                <button class="btn btn-outline-primary prev-step" data-prev="2">Назад</button>
                                <button class="btn btn-primary next-step" data-next="4">Далее</button>
                            </div>
                        </div>

                        <!-- Шаг 4: Подтверждение -->
                        <div class="step-content" data-step="4">
                            <div class="glass-card p-4 mb-4">
                                <h3 class="mb-4">Подтверждение заказа</h3>
                                <div class="order-summary-preview">
                                    <h5 class="mb-4">Сводка заказа</h5>
                                    <div class="summary-item">
                                        <span>Услуга:</span>
                                        <span id="summary-service">Создание видео</span>
                                    </div>
                                    <div class="summary-item">
                                        <span>Тип услуги:</span>
                                        <span id="summary-service-type">Промо-ролик</span>
                                    </div>
                                    <div class="summary-item">
                                        <span>Стиль:</span>
                                        <span id="summary-style">Современный</span>
                                    </div>
                                    <div class="summary-item">
                                        <span>Дополнительные опции:</span>
                                        <span id="summary-options">Нет</span>
                                    </div>
                                    <div class="summary-total">
                                        <span>Итого:</span>
                                        <span id="summary-total">500 ₽</span>
                                    </div>
                                </div>
                                <div class="mt-4">
                                    <div class="form-check">
                                        <input class="form-check-input" type="checkbox" id="agree-terms" required>
                                        <label class="form-check-label" for="agree-terms">
                                            Я согласен с условиями предоставления услуг и политикой конфиденциальности
                                        </label>
                                    </div>
                                </div>
                            </div>
                            <div class="constructor-navigation">
                                <button class="btn btn-outline-primary prev-step" data-prev="3">Назад</button>
                                <button class="btn btn-success" id="submit-order">Отправить заказ</button>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-4">
                        <div class="order-summary-preview">
                            <div class="floating-badge">Активно</div>
                            <h4 class="mb-4">Ваш заказ</h4>
                            <div class="summary-item">
                                <span>Текущий шаг:</span>
                                <span id="current-step">Выбор услуги</span>
                            </div>
                            <div class="summary-item">
                                <span>Выбранная услуга:</span>
                                <span id="selected-service-preview">Не выбрана</span>
                            </div>
                            <div class="summary-item">
                                <span>Тип услуги:</span>
                                <span id="selected-service-type-preview">-</span>
                            </div>
                            <div class="summary-item">
                                <span>Стоимость:</span>
                                <span id="estimated-price">0 ₽</span>
                            </div>
                            <div class="summary-total">
                                <span>Прогресс:</span>
                                <span id="progress-percent">0%</span>
                            </div>
                            <div class="progress mt-2" style="height: 8px;">
                                <div class="progress-bar" role="progressbar" style="width: 0%;" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
                            </div>
                            <div class="alert alert-info mt-3">
                                <i class="fas fa-info-circle me-2"></i>
                                После подтверждения заказа откроется Telegram для уточнения деталей
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- НОВАЯ СТРАНИЦА GALAXY STARS & PREMIUM -->
    <div id="stars" class="page page-transition">
        <section class="galaxy-hero">
            <div class="galaxy-bg"></div>
            <div class="galaxy-stars">
                <div class="galaxy-star"></div>
                <div class="galaxy-star"></div>
                <div class="galaxy-star"></div>
                <div class="galaxy-star"></div>
                <div class="galaxy-star"></div>
            </div>
            <div class="container">
                <div class="row justify-content-center text-center">
                    <div class="col-lg-8">
                        <h1 class="galaxy-title">Galaxy Stars & Premium</h1>
                        <p class="galaxy-subtitle">Приобретайте звёзды и Premium подписку для своего Telegram аккаунта легко и безопасно через нашего бота</p>
                        <button class="galaxy-stars-btn" id="premium-features-btn">
                            <i class="fas fa-arrow-down me-2"></i>Эксклюзивный доступ к премиум функциям
                        </button>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="py-5">
            <div class="container">
                <div class="row">
                    <div class="col-lg-4 mb-4">
                        <div class="galaxy-card">
                            <div class="galaxy-icon">
                                <i class="fas fa-star"></i>
                            </div>
                            <h3 class="text-center mb-3">Telegram Stars</h3>
                            <p class="text-center">Поддерживайте создателей контента и увеличивайте видимость вашего канала</p>
                            <div class="galaxy-badge text-center">Безопасно и конфиденциально</div>
                        </div>
                    </div>
                    <div class="col-lg-4 mb-4">
                        <div class="galaxy-card">
                            <div class="galaxy-icon">
                                <i class="fas fa-crown"></i>
                            </div>
                            <h3 class="text-center mb-3">Telegram Premium</h3>
                            <p class="text-center">Расширенные функции, эксклюзивный контент и улучшенные настройки приватности</p>
                            <div class="galaxy-badge text-center">Эксклюзивные возможности</div>
                        </div>
                    </div>
                    <div class="col-lg-4 mb-4">
                        <div class="galaxy-card">
                            <div class="galaxy-icon">
                                <i class="fas fa-bolt"></i>
                            </div>
                            <h3 class="text-center mb-3">Мгновенная доставка</h3>
                            <p class="text-center">Звёзды зачисляются в течение 3-7 минут после успешной оплаты</p>
                            <div class="galaxy-badge text-center">Быстро и надежно</div>
                        </div>
                    </div>
                </div>
                
                <div class="galaxy-steps" id="premium-steps">
                    <div class="galaxy-step">
                        <div class="galaxy-step-number">1</div>
                        <div class="galaxy-step-content">
                            <div class="galaxy-step-title">Перейдите в нашего бота</div>
                            <div class="galaxy-step-description">Нажмите кнопку "Перейти к боту" ниже, чтобы открыть Telegram бота для покупки звезд.</div>
                        </div>
                    </div>
                    <div class="galaxy-step">
                        <div class="galaxy-step-number">2</div>
                        <div class="galaxy-step-content">
                            <div class="galaxy-step-title">Пополните баланс</div>
                            <div class="galaxy-step-description">В боте нажмите кнопку "Пополнить баланс" и выберите удобный способ оплаты.</div>
                        </div>
                    </div>
                    <div class="galaxy-step">
                        <div class="galaxy-step-number">3</div>
                        <div class="galaxy-step-content">
                            <div class="galaxy-step-title">Купите Telegram Stars/Premium</div>
                            <div class="galaxy-step-description">После пополнения баланса нажмите кнопку "Купить Telegram Stars/Premium"</div>
                        </div>
                    </div>
                    <div class="galaxy-step">
                        <div class="galaxy-step-number">4</div>
                        <div class="galaxy-step-content">
                            <div class="galaxy-step-title">Выберите получателя</div>
                            <div class="galaxy-step-description">Укажите, кому вы хотите купить звёзды/Premium: для своего аккаунта или для друга</div>
                        </div>
                    </div>
                    <div class="galaxy-step">
                        <div class="galaxy-step-number">5</div>
                        <div class="galaxy-step-content">
                            <div class="galaxy-step-title">Введите количество</div>
                            <div class="galaxy-step-description">Введите необходимое количество звёзд и подтвердите покупку.</div>
                        </div>
                    </div>
                    <div class="galaxy-step">
                        <div class="galaxy-step-number">6</div>
                        <div class="galaxy-step-content">
                            <div class="galaxy-step-title">Получите звёзды</div>
                            <div class="galaxy-step-description">После успешной оплаты звёзды будут зачислены в течение 3-7 минут.</div>
                        </div>
                    </div>
                </div>
                
                <div class="text-center mt-5">
                    <a href="https://t.me/st1xloxstars_bot" target="_blank" class="galaxy-btn">
                        <i class="fab fa-telegram me-2"></i>Приобрести звёзды/Premium
                    </a>
                </div>
            </div>
        </section>
    </div>

    <!-- УЛУЧШЕННАЯ СТРАНИЦА "О НАС" -->
    <div id="about" class="page page-transition">
        <section class="about-hero-modern">
            <div class="container">
                <div class="row align-items-center">
                    <div class="col-lg-6">
                        <h1 class="display-4 fw-bold mb-4">О нас</h1>
                        <p class="hero-subtitle">Мы команда профессионалов, специализирующаяся на создании уникальных цифровых решений для бизнеса и личных проектов.</p>
                    </div>
                    <div class="col-lg-6 text-center">
                        <div class="glass-card p-4 floating-element">
                            <i class="fas fa-users display-1 text-accent mb-3"></i>
                            <h3>Наша миссия</h3>
                            <p>Помогать нашим клиентам достигать их целей с помощью инновационных решений и креативного подхода.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="py-5">
            <div class="container">
                <div class="stats-counter">
                    <div class="stat-item">
                        <div class="stat-number" id="clients-count">150+</div>
                        <div class="stat-label">Довольных клиентов</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number" id="projects-count">300+</div>
                        <div class="stat-label">Выполненных проектов</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number" id="experience-count">3+</div>
                        <div class="stat-label">Года опыта</div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- УЛУЧШЕННЫЙ РАЗДЕЛ TELEGRAM -->
        <section class="about-telegram-section">
            <div class="container">
                <h2 class="text-center mb-5">Наши Telegram ресурсы</h2>
                
                <div class="about-telegram-grid">
                    <div class="telegram-card-modern">
                        <div class="telegram-card-header">
                            <i class="fab fa-telegram telegram-card-icon"></i>
                            <h4 class="mb-0">st1xiox Channel</h4>
                        </div>
                        <div class="telegram-card-content">
                            <p class="telegram-card-description">Наш официальный канал с эксклюзивным контентом, полезными советами и новостями о наших услугах.</p>
                            <a href="https://t.me/zxcst1xlox" target="_blank" class="btn btn-primary w-100">
                                <i class="fab fa-telegram me-2"></i>Подписаться на канал
                            </a>
                        </div>
                    </div>
                    
                    <div class="telegram-card-modern">
                        <div class="telegram-card-header">
                            <i class="fas fa-comments telegram-card-icon"></i>
                            <h4 class="mb-0">st1xiox Chat</h4>
                        </div>
                        <div class="telegram-card-content">
                            <p class="telegram-card-description">Присоединяйтесь к нашему чату для общения с другими участниками и получения поддержки.</p>
                            <a href="https://t.me/+iTm2LIDyzmk5NDMy" target="_blank" class="btn btn-primary w-100">
                                <i class="fab fa-telegram me-2"></i>Присоединиться к чату
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- СВЯЗЬ С АДМИНИСТРАЦИЕЙ -->
                <div class="contact-admin-modern">
                    <h3>Связь с администрацией</h3>
                    <p class="mb-4">Есть вопросы или предложения? Свяжитесь с нашей администрацией напрямую через Telegram</p>
                    <div class="glass-card p-4 mt-4">
                        <div class="mb-3">
                            <label class="form-label">Ваш Email</label>
                            <input type="email" class="form-control" placeholder="example@email.com">
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Ваш Telegram @username</label>
                            <input type="text" class="form-control" placeholder="@username">
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Ваше сообщение</label>
                            <textarea class="form-control" rows="4" placeholder="Привет, я хочу заказать..."></textarea>
                        </div>
                        <a href="https://t.me/st1xloxServices_bot" target="_blank" class="btn btn-accent w-100">
                            <i class="fab fa-telegram me-2"></i>Отправить в Telegram
                        </a>
                    </div>
                </div>
            </div>
        </section>
    </div>

     <!-- Страница отзывов - БЕЗ ФОРМЫ ОТЗЫВА -->
    <div id="reviews" class="page">
        <div class="container py-5">
            <h1 class="text-center mb-5">Отзывы наших клиентов</h1>
            
            <div class="reviews-carousel">
                <div class="reviews-carousel-inner" id="reviews-carousel-inner">
                    <!-- Отзывы будут загружены через JavaScript -->
                </div>
                <div class="carousel-controls">
                    <button class="carousel-control" id="carousel-prev">
                        <i class="fas fa-chevron-left"></i>
                    </button>
                    <button class="carousel-control" id="carousel-next">
                        <i class="fas fa-chevron-right"></i>
                    </button>
                </div>
            </div>
            
            <!-- УБРАНА ФОРМА ОТЗЫВА -->
        </div>
    </div>

    <!-- УЛУЧШЕННЫЙ AI ЧАТ -->
    <div id="chat" class="page page-transition">
        <div class="container py-5">
            <h1 class="text-center mb-5">st1xlox AI-Chat</h1>
            
            <div class="row justify-content-center">
                <div class="col-lg-10">
                    <div class="ai-chat-container">
                        <div class="ai-chat-header">
                            <h2 class="ai-chat-title">Умный помощник st1xlox AI</h2>
                        </div>
                        <div class="ai-chat-body" id="ai-chat-body">
                            <div class="ai-message bot">
                                Привет! Я st1xlox AI - ваш умный помощник. Могу ответить на любой ваш вопрос о наших услугах или просто поддержать беседу!
                            </div>
                        </div>
                        <div class="ai-quick-replies" id="ai-quick-replies">
                            <button class="quick-reply-btn" data-message="Какие услуги вы предоставляете?">Услуги</button>
                            <button class="quick-reply-btn" data-message="Сколько стоит реклама в Telegram?">Цены на рекламу</button>
                            <button class="quick-reply-btn" data-message="Как купить Telegram Stars?">Покупка Stars</button>
                            <button class="quick-reply-btn" data-message="Какие сроки выполнения заказов?">Сроки</button>
                        </div>
                        <div class="ai-chat-input">
                            <input type="text" class="chat-input" id="ai-chat-input" placeholder="Задайте любой вопрос...">
                            <button class="send-btn" id="ai-send-btn">
                                <i class="fas fa-paper-plane"></i>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- СТРАНИЦА ВХОДА С КАПЧЕЙ -->
    <div id="login" class="page page-transition">
        <div class="auth-form-container">
            <div id="particles-js"></div>
            <div class="container">
                <div class="row justify-content-center">
                    <div class="col-md-6 col-lg-5">
                        <div class="auth-card">
                            <div class="auth-header">
                                <h2 class="auth-title">Вход в аккаунт</h2>
                                <p class="auth-subtitle">Добро пожаловать обратно!</p>
                            </div>
                            <div class="auth-body">
                                <form id="login-form">
                                    <div class="form-group">
                                        <input type="email" class="form-input" id="login-email" placeholder=" " required>
                                        <label class="form-label" for="login-email">Email</label>
                                    </div>
                                    <div class="form-group">
                                        <input type="password" class="form-input" id="login-password" placeholder=" " required>
                                        <label class="form-label" for="login-password">Пароль</label>
                                    </div>
                                    <div class="captcha-container">
                                        <div class="captcha-text" id="login-captcha-text">A1B2C</div>
                                        <input type="text" class="captcha-input" id="login-captcha-input" placeholder="Введите код" required>
                                    </div>
                                    <div class="form-check mb-4">
                                        <input type="checkbox" class="form-check-input" id="remember-me">
                                        <label class="form-check-label" for="remember-me">Запомнить меня</label>
                                    </div>
                                    <button type="submit" class="btn btn-primary w-100 mb-3">Войти</button>
                                </form>
                            </div>
                            <div class="auth-footer">
                                <p>Нет аккаунта? <a href="#" class="auth-link" data-page="register">Зарегистрироваться</a></p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- СТРАНИЦА РЕГИСТРАЦИИ С КАПЧЕЙ -->
    <div id="register" class="page page-transition">
        <div class="auth-form-container">
            <div id="particles-js-register"></div>
            <div class="container">
                <div class="row justify-content-center">
                    <div class="col-md-6 col-lg-5">
                        <div class="auth-card">
                            <div class="auth-header">
                                <h2 class="auth-title">Регистрация</h2>
                                <p class="auth-subtitle">Создайте новый аккаунт</p>
                            </div>
                            <div class="auth-body">
                                <form id="register-form">
                                    <div class="form-group">
                                        <input type="text" class="form-input" id="register-name" placeholder=" " required>
                                        <label class="form-label" for="register-name">Имя</label>
                                    </div>
                                    <div class="form-group">
                                        <input type="email" class="form-input" id="register-email" placeholder=" " required>
                                        <label class="form-label" for="register-email">Email</label>
                                    </div>
                                    <div class="form-group">
                                        <input type="password" class="form-input" id="register-password" placeholder=" " required>
                                        <label class="form-label" for="register-password">Пароль</label>
                                    </div>
                                    <div class="form-group">
                                        <input type="password" class="form-input" id="register-confirm-password" placeholder=" " required>
                                        <label class="form-label" for="register-confirm-password">Подтверждение пароля</label>
                                    </div>
                                    <div class="captcha-container">
                                        <div class="captcha-text" id="register-captcha-text">X3Y4Z</div>
                                        <input type="text" class="captcha-input" id="register-captcha-input" placeholder="Введите код" required>
                                    </div>
                                    <div class="form-check mb-4">
                                        <input type="checkbox" class="form-check-input" id="agree-terms-register" required>
                                        <label class="form-check-label" for="agree-terms-register">Я согласен с условиями использования</label>
                                    </div>
                                    <button type="submit" class="btn btn-primary w-100 mb-3">Зарегистрироваться</button>
                                </form>
                            </div>
                            <div class="auth-footer">
                                <p>Уже есть аккаунт? <a href="#" class="auth-link" data-page="login">Войти</a></p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- НОВЫЙ УЛУЧШЕННЫЙ ЛИЧНЫЙ КАБИНЕТ -->
    <div id="dashboard" class="page page-transition">
        <div class="new-dashboard">
            <div class="container">
                <div class="dashboard-header">
                    <div>
                        <h1 class="dashboard-welcome" id="dashboard-welcome">Добро пожаловать!</h1>
                        <p class="text-muted" id="dashboard-date">Сегодня <span id="current-date"></span></p>
                    </div>
                    <div class="d-flex align-items-center">
                        <div class="me-3">
                            <div class="user-avatar" id="dashboard-user-avatar" style="cursor: pointer;" data-bs-toggle="modal" data-bs-target="#avatarUploadModal">
                                U
                            </div>
                        </div>
                    </div>
                </div>

                <div class="dashboard-stats-cards">
                    <div class="dashboard-stat-card">
                        <div class="dashboard-stat-icon">
                            <i class="fas fa-shopping-cart"></i>
                        </div>
                        <div class="dashboard-stat-number" id="dashboard-orders-count">0</div>
                        <div class="dashboard-stat-label">Всего заказов</div>
                    </div>
                    <div class="dashboard-stat-card">
                        <div class="dashboard-stat-icon">
                            <i class="fas fa-check-circle"></i>
                        </div>
                        <div class="dashboard-stat-number" id="dashboard-completed-orders">0</div>
                        <div class="dashboard-stat-label">Выполнено</div>
                    </div>
                    <div class="dashboard-stat-card">
                        <div class="dashboard-stat-icon">
                            <i class="fas fa-star"></i>
                        </div>
                        <div class="dashboard-stat-number" id="dashboard-reviews-count">0</div>
                        <div class="dashboard-stat-label">Отзывов</div>
                    </div>
                    <div class="dashboard-stat-card">
                        <div class="dashboard-stat-icon">
                            <i class="fas fa-wallet"></i>
                        </div>
                        <div class="dashboard-stat-number" id="dashboard-total-spent">0 ₽</div>
                        <div class="dashboard-stat-label">Потрачено</div>
                    </div>
                </div>

                <div class="dashboard-content">
                    <div class="profile-section">
                        <div class="profile-avatar-section">
                            <div class="profile-avatar-large" id="profile-avatar-large" data-bs-toggle="modal" data-bs-target="#avatarUploadModal">
                                <i class="fas fa-user" style="font-size: 3rem; color: rgba(255,255,255,0.5);"></i>
                            </div>
                            <button class="avatar-upload-btn" data-bs-toggle="modal" data-bs-target="#avatarUploadModal">
                                <i class="fas fa-camera me-2"></i>Изменить аватар
                            </button>
                        </div>

                        <div class="profile-info-section">
                            <div class="profile-name" id="profile-name">Пользователь</div>
                            <div class="profile-email" id="profile-email">user@example.com</div>
                            <div class="d-flex align-items-center mt-2">
                                <span class="badge bg-success me-2">● Активен</span>
                                <span class="text-muted" id="profile-registration-date">Зарегистрирован: 01.01.2023</span>
                            </div>
                        </div>

                        <div class="profile-badges-section">
                            <div class="profile-badge-new">
                                <i class="fas fa-medal me-1"></i> Новичок
                            </div>
                            <div class="profile-badge-new">
                                <i class="fas fa-star me-1"></i> Активный
                            </div>
                            <div class="profile-badge-new">
                                <i class="fas fa-check me-1"></i> Подтвержден
                            </div>
                        </div>

                        <div class="profile-actions-section">
                            <button class="profile-action-btn" id="edit-profile-btn">
                                <i class="fas fa-edit me-2"></i> Редактировать
                            </button>
                            <button class="profile-action-btn" id="settings-btn">
                                <i class="fas fa-cog me-2"></i> Настройки
                            </button>
                        </div>
                    </div>

                    <div class="orders-section">
                        <div class="orders-header">
                            <div class="orders-title">История заказов</div>
                            <select class="orders-filter" id="orders-filter">
                                <option value="all">Все заказы</option>
                                <option value="completed">Выполненные</option>
                                <option value="pending">В обработке</option>
                            </select>
                        </div>

                        <div class="orders-list" id="orders-list">
                            <!-- Заказы будут загружены через JavaScript -->
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- УЛУЧШЕННАЯ АДМИН ПАНЕЛЬ -->
    <div id="admin" class="page page-transition">
        <div class="container py-5">
            <h1 class="text-center mb-5">Административная панель</h1>
            
            <!-- Быстрые действия -->
            <div class="admin-quick-actions mb-5">
                <div class="admin-quick-action" id="quick-users">
                    <div class="admin-quick-action-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h5>Управление пользователями</h5>
                    <p>Просмотр, редактирование и управление пользователями</p>
                </div>
                <div class="admin-quick-action" id="quick-orders">
                    <div class="admin-quick-action-icon">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <h5>Управление заказами</h5>
                    <p>Просмотр и управление всеми заказами</p>
                </div>
                <div class="admin-quick-action" id="quick-revenue">
                    <div class="admin-quick-action-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h5>Аналитика доходов</h5>
                    <p>Подробная статистика и аналитика доходов</p>
                </div>
                <div class="admin-quick-action" id="quick-reviews">
                    <div class="admin-quick-action-icon">
                        <i class="fas fa-star"></i>
                    </div>
                    <h5>Модерация отзывов</h5>
                    <p>Проверка и публикация отзывов</p>
                </div>
            </div>
            
            <!-- Улучшенная статистика -->
            <div class="admin-dashboard">
                <div class="admin-widget">
                    <div class="admin-widget-header">
                        <div class="admin-widget-title">Пользователи</div>
                        <div class="admin-widget-value" id="admin-total-users">0</div>
                    </div>
                    <p>Зарегистрировано пользователей</p>
                    <div class="admin-action-buttons">
                        <button class="admin-action-btn" id="admin-view-users-btn">
                            <i class="fas fa-users me-2"></i>Просмотреть всех
                        </button>
                        <button class="admin-action-btn" id="admin-add-user-btn">
                            <i class="fas fa-plus me-2"></i>Добавить
                        </button>
                    </div>
                </div>
                
                <div class="admin-widget">
                    <div class="admin-widget-header">
                        <div class="admin-widget-title">Заказы</div>
                        <div class="admin-widget-value" id="admin-total-orders">0</div>
                    </div>
                    <p>Активных заказов: <span id="admin-active-orders">0</span></p>
                    <div class="admin-action-buttons">
                        <button class="admin-action-btn" id="admin-all-orders-btn">
                            <i class="fas fa-list me-2"></i>Все заказы
                        </button>
                        <button class="admin-action-btn" id="admin-new-orders-btn">
                            <i class="fas fa-bell me-2"></i>Новые
                        </button>
                    </div>
                </div>
                
                <div class="admin-widget">
                    <div class="admin-widget-header">
                        <div class="admin-widget-title">Доход</div>
                        <div class="admin-widget-value" id="admin-total-revenue">0 руб.</div>
                    </div>
                    <p>За текущий месяц: <span id="admin-month-revenue">0 руб.</span></p>
                    <div class="admin-action-buttons">
                        <button class="admin-action-btn" id="admin-revenue-report-btn">
                            <i class="fas fa-chart-bar me-2"></i>Отчет
                        </button>
                        <button class="admin-action-btn" id="admin-export-revenue-btn">
                            <i class="fas fa-download me-2"></i>Экспорт
                        </button>
                    </div>
                </div>
                
                <div class="admin-widget">
                    <div class="admin-widget-header">
                        <div class="admin-widget-title">Отзывы</div>
                        <div class="admin-widget-value" id="admin-total-reviews">0</div>
                    </div>
                    <p>На модерации: <span id="admin-pending-reviews">0</span></p>
                    <div class="admin-action-buttons">
                        <button class="admin-action-btn" id="admin-all-reviews-btn">
                            <i class="fas fa-star me-2"></i>Все отзывы
                        </button>
                        <button class="admin-action-btn" id="admin-moderate-reviews-btn">
                            <i class="fas fa-check-circle me-2"></i>Модерация
                        </button>
                    </div>
                </div>
            </div>

            <!-- Управление пользователями -->
            <div class="admin-table-container">
                <div class="admin-table-header">
                    <h3 class="mb-0">Управление пользователями</h3>
                    <div class="d-flex gap-3">
                        <input type="text" class="admin-search-box" placeholder="Поиск пользователей..." id="user-search">
                        <button class="btn btn-primary" id="admin-add-user-btn2">Добавить пользователя</button>
                    </div>
                </div>
                <div class="table-responsive">
                    <table class="table table-hover">
                        <thead>
                            <tr>
                                <th>ID</th>
                                <th>Имя</th>
                                <th>Email</th>
                                <th>Роль</th>
                                <th>Дата регистрации</th>
                                <th>Статус</th>
                                <th>Действия</th>
                            </tr>
                        </thead>
                        <tbody id="users-table">
                            <!-- Пользователи будут загружены через JavaScript -->
                        </tbody>
                    </table>
                </div>
            </div>
            
            <!-- Управление заказами -->
            <div class="admin-table-container">
                <div class="admin-table-header">
                    <h3 class="mb-0">Управление заказами</h3>
                    <div class="btn-group">
                        <button class="btn btn-outline-primary active" data-order-filter="all">Все</button>
                        <button class="btn btn-outline-primary" data-order-filter="pending">В обработке</button>
                        <button class="btn btn-outline-primary" data-order-filter="completed">Завершенные</button>
                    </div>
                </div>
                <div class="table-responsive">
                    <table class="table table-hover">
                        <thead>
                            <tr>
                                <th>ID</th>
                                <th>Пользователь</th>
                                <th>Тип заказа</th>
                                <th>Дата</th>
                                <th>Стоимость</th>
                                <th>Статус</th>
                                <th>Действия</th>
                            </tr>
                        </thead>
                        <tbody id="orders-table">
                            <!-- Заказы будут загружены через JavaScript -->
                        </tbody>
                    </table>
                </div>
            </div>

            <!-- Управление отзывами -->
            <div class="admin-table-container">
                <h3 class="mb-4">Управление отзывами</h3>
                <div class="table-responsive">
                    <table class="table table-hover">
                        <thead>
                            <tr>
                                <th>ID</th>
                                <th>Автор</th>
                                <th>Текст</th>
                                <th>Оценка</th>
                                <th>Дата</th>
                                <th>Статус</th>
                                <th>Действия</th>
                            </tr>
                        </thead>
                        <tbody id="reviews-table">
                            <!-- Отзывы будут загружены через JavaScript -->
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>

    <!-- Sticky кнопка для Galaxy Stars -->
    <div class="sticky-galaxy-btn">
        <button class="galaxy-stars-btn" id="sticky-galaxy-btn">
            <i class="fas fa-star me-2"></i>Galaxy Stars
        </button>
    </div>

    <!-- Footer -->
    <footer class="py-4 mt-5">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <h5>st1xlox Services</h5>
                    <p>Профессиональные услуги для развития вашего бренда и бизнеса</p>
                </div>
                <div class="col-md-3">
                    <h5>Контакты</h5>
                    <ul class="list-unstyled">
                        <li><a href="https://t.me/st1xlox" target="_blank" class="text-light">Telegram: @st1xlox</a></li>
                        <li><a href="mailto:info@st1xlox.com" class="text-light">info@st1xlox.com</a></li>
                    </ul>
                </div>
                <div class="col-md-3">
                    <h5>Быстрые ссылки</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" data-page="home" class="text-light">Главная</a></li>
                        <li><a href="#" data-page="orders" class="text-light">Оформление заказа</a></li>
                        <li><a href="#" data-page="stars" class="text-light">Galaxy Stars&Premium</a></li>
                        <li><a href="#" data-page="about" class="text-light">О нас</a></li>
                    </ul>
                </div>
            </div>
            <hr class="my-4">
            <div class="text-center">
                <p>&copy; 2025 st1xlox Services. Все права защищены.</p>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
    <script>
        // Инициализация частиц для фона
        document.addEventListener('DOMContentLoaded', function() {
            if (typeof particlesJS !== 'undefined') {
                particlesJS('particles-js', {
                    particles: {
                        number: { value: 80, density: { enable: true, value_area: 800 } },
                        color: { value: "#b967ff" },
                        shape: { type: "circle" },
                        opacity: { value: 0.5, random: true },
                        size: { value: 3, random: true },
                        line_linked: {
                            enable: true,
                            distance: 150,
                            color: "#b967ff",
                            opacity: 0.4,
                            width: 1
                        },
                        move: {
                            enable: true,
                            speed: 2,
                            direction: "none",
                            random: true,
                            straight: false,
                            out_mode: "out",
                            bounce: false
                        }
                    },
                    interactivity: {
                        detect_on: "canvas",
                        events: {
                            onhover: { enable: true, mode: "repulse" },
                            onclick: { enable: true, mode: "push" },
                            resize: true
                        }
                    }
                });

                particlesJS('particles-js-register', {
                    particles: {
                        number: { value: 80, density: { enable: true, value_area: 800 } },
                        color: { value: "#ff2a6d" },
                        shape: { type: "circle" },
                        opacity: { value: 0.5, random: true },
                        size: { value: 3, random: true },
                        line_linked: {
                            enable: true,
                            distance: 150,
                            color: "#ff2a6d",
                            opacity: 0.4,
                            width: 1
                        },
                        move: {
                            enable: true,
                            speed: 2,
                            direction: "none",
                            random: true,
                            straight: false,
                            out_mode: "out",
                            bounce: false
                        }
                    },
                    interactivity: {
                        detect_on: "canvas",
                        events: {
                            onhover: { enable: true, mode: "repulse" },
                            onclick: { enable: true, mode: "push" },
                            resize: true
                        }
                    }
                });
            }
        });

        // УЛУЧШЕННЫЙ AI - МОЖЕТ ОТВЕЧАТЬ НА ЛЮБЫЕ ВОПРОСЫ С РАЗНЫМИ ВАРИАНТАМИ ОТВЕТОВ
        const ultraAI = {
            // База знаний для ответов на конкретные вопросы с вариациями
            knowledgeBase: {
                "привет": [
                    "Привет! Я st1xlox AI - умный помощник. Рад тебя видеть! Чем могу помочь?",
                    "Здравствуйте! Я st1xlox AI, ваш персональный помощник. Задавайте любые вопросы!",
                    "Приветствую! Я искусственный интеллект st1xlox Services. Готов помочь вам с любыми вопросами!"
                ],
                "здравствуйте": [
                    "Здравствуйте! Я st1xlox AI, ваш персональный помощник. Задавайте любые вопросы!",
                    "Добрый день! Рад вас видеть. Чем могу быть полезен?",
                    "Приветствую! Я AI-помощник st1xlox Services. Готов ответить на ваши вопросы!"
                ],
                "как дела": [
                    "У меня всё отлично! Я готов помочь вам с любыми вопросами о наших услугах или вообще о чём угодно!",
                    "Спасибо, что спросили! У меня всё прекрасно, я работаю на полную мощность. А как ваши дела?",
                    "Всё замечательно! Готов к работе и жду ваших вопросов о наших услугах!"
                ],
                "кто ты": [
                    "Я st1xlox AI - умный искусственный интеллект, созданный для помощи нашим клиентам. Я могу ответить на любой ваш вопрос!",
                    "Я - виртуальный помощник st1xlox Services, созданный на основе передовых технологий искусственного интеллекта.",
                    "Я AI-ассистент команды st1xlox, готовый помочь вам с информацией о наших услугах и не только!"
                ],
                "расскажи о себе": [
                    "Конечно! Я st1xlox AI - передовой искусственный интеллект, созданный командой st1xlox Services. Моя задача - помогать клиентам, отвечать на вопросы и предоставлять информацию о наших услугах. Я постоянно учусь и развиваюсь!",
                    "Я - умный помощник, созданный специально для st1xlox Services. Могу ответить на вопросы о наших услугах, помочь с оформлением заказов или просто поддержать беседу!",
                    "Я виртуальный ассистент st1xlox Services, оснащенный передовыми алгоритмами искусственного интеллекта. Моя цель - сделать ваше взаимодействие с нашими услугами максимально комфортным и эффективным!"
                ],
                "какие услуги ты предоставляешь": [
                    "Мы предоставляем широкий спектр услуг для Telegram:\n- Покупка звёзд для каналов\n- Рекламные кампании\n- Создание контента (видео, изображения)\n- Разработка аватарок\n- Привлечение подписчиков\nИ многое другое!",
                    "Наши основные услуги включают:\n• Продвижение Telegram-каналов\n• Создание качественного контента\n• Рекламные кампании в социальных сетях\n• Привлечение целевой аудитории\n• Разработка уникального визуального стиля",
                    "st1xlox Services предлагает:\n- Профессиональное продвижение в Telegram\n- Создание креативного контента\n- Эффективные рекламные стратегии\n- Увеличение вовлеченности аудитории\n- Разработка индивидуальных решений для вашего бренда"
                ],
                "как купить звезды": [
                    "Покупка звёзд для Telegram очень проста:\n1. Перейдите в нашего бота @st1xloxstars_bot\n2. Выберите количество звёзд\n3. Оплатите удобным способом\n4. Получите звёзды на ваш канал\nВсё безопасно и конфиденциально!",
                    "Чтобы приобрести звёзды для вашего Telegram-канала:\n1. Откройте нашего бота @st1xloxstars_bot\n2. Выберите подходящий пакет звёзд\n3. Совершите оплату\n4. Звёзды будут доставлены в течение 24 часов\nЭто быстро, просто и безопасно!",
                    "Процесс покупки звёзд:\n• Найти бота @st1xloxstars_bot в Telegram\n• Выбрать нужное количество звёзд\n• Оплатить выбранным способом\n• Получить звёзды на канал\nМы гарантируем безопасность и конфиденциальность каждой транзакции!"
                ],
                "сколько стоит реклама": [
                    "Стоимость рекламы зависит от многих факторов:\n- Платформа (Telegram, Instagram, YouTube)\n- Продолжительность кампании\n- Целевая аудитория\n- Бюджет\nРекомендую оформить заказ для точного расчёта!",
                    "Цена на рекламные услуги варьируется в зависимости от:\n• Выбранной платформы продвижения\n• Длительности рекламной кампании\n• Размера целевой аудитории\n• Сложности реализации\nДля точного расчета стоимости лучше оформить заказ!",
                    "Стоимость рекламы определяется несколькими параметрами:\n- Социальная сеть для продвижения\n- Продолжительность размещения\n- Охват целевой аудитории\n- Специфика контента\nРекомендую обратиться к нам для детального расчета!"
                ],
                "как связаться с поддержкой": [
                    "Вы можете связаться с нами:\n- Через этот чат\n- В Telegram: @st1xlox\n- По email: info@st1xlox.com\n- В нашем Telegram-чате: https://t.me/+iTm2LIDyzmk5NDMy",
                    "Связаться с поддержкой можно несколькими способами:\n• Написать в этот чат\n• Написать в Telegram: @st1xlox\n• Отправить email на info@st1xlox.com\n• Присоединиться к нашему чату: https://t.me/+iTm2LIDyzmk5NDMy",
                    "Для связи с поддержкой используйте:\n- Этот AI-чат\n- Telegram: @st1xlox\n- Электронную почту: info@st1xlox.com\n- Наш Telegram-чат: https://t.me/+iTm2LIDyzmk5NDMy\nМы всегда рады помочь!"
                ],
                "есть ли скидки": [
                    "Конечно! У нас регулярно проходят акции:\n- 10% скидка новым клиентам\n- Специальные предложения для постоянных клиентов\n- Сезонные акции и распродажи\nСледите за нашим каналом @zxcst1xlox!",
                    "Да, мы предлагаем различные скидки:\n• 10% для новых клиентов\n• Накопительные скидки для постоянных заказчиков\n• Сезонные акции и специальные предложения\n• Партнерская программа со скидками\nПодписывайтесь на @zxcst1xlox чтобы не пропустить акции!",
                    "У нас есть система скидок:\n- Приветственная скидка 10% для новых клиентов\n- Накопительная система для постоянных заказчиков\n- Сезонные распродажи и акции\n- Специальные условия для партнеров\nСледите за обновлениями в @zxcst1xlox!"
                ],
                "сколько времени выполняется заказ": [
                    "Сроки выполнения зависят от типа заказа:\n- Звёзды: 1-24 часа\n- Реклама: 1-3 дня\n- Видео/изображения: 3-7 дней\nТочные сроки уточняются при оформлении.",
                    "Время выполнения заказов:\n• Покупка звёзд - 1-24 часа\n• Рекламные кампании - 1-3 рабочих дня\n• Создание контента - 3-7 дней\n• Индивидуальные проекты - обсуждается отдельно\nТочные сроки указываются при подтверждении заказа!",
                    "Стандартные сроки выполнения:\n- Звёзды для Telegram: до 24 часов\n- Рекламные кампании: 1-3 дня\n- Видео и изображения: 3-7 дней\n- Сложные проекты: индивидуально\nКонкретные сроки уточняются при оформлении заказа!"
                ],
                "гарантии": [
                    "Мы предоставляем полные гарантии:\n- Безопасность всех методов\n- Конфиденциальность данных\n- Возврат средств при невозможности выполнения\n- Поддержка 24/7\n- Качественное выполнение работ",
                    "Наши гарантии включают:\n• Полную безопасность используемых методов\n• Строгую конфиденциальность данных\n• Возврат средств в случае невыполнения обязательств\n• Круглосуточную поддержку\n• Высокое качество предоставляемых услуг",
                    "Мы гарантируем:\n- Безопасность и надежность всех услуг\n- Полную конфиденциальность информации\n- Возврат средств при невозможности выполнения заказа\n- Поддержку 24/7\n- Профессиональное выполнение работ"
                ],
                "спасибо": [
                    "Пожалуйста! Всегда рад помочь! Если возникнут ещё вопросы - обращайтесь! 😊",
                    "Не стоит благодарности! Обращайтесь в любое время, буду рад помочь снова! 🚀",
                    "Рад был помочь! Если понадобится дополнительная информация - не стесняйтесь спрашивать! 💫"
                ],
                "пока": [
                    "До свидания! Ждём вас снова! Удачи! 🚀",
                    "Всего хорошего! Надеюсь увидеть вас снова! ✨",
                    "До новых встреч! Успехов в ваших проектах! 🌟"
                ],
                "что такое telegram звезды": [
                    "Telegram звёзды - это внутренняя валюта Telegram, которая позволяет поддерживать создателей контента. Покупая звёзды для своего канала, вы увеличиваете его видимость и привлекаете больше подписчиков!",
                    "Telegram Stars - это специальная валюта платформы для поддержки авторов контента. Приобретение звёзд помогает продвижению канала, увеличивает его популярность и привлекает новую аудиторию!",
                    "Звёзды в Telegram - это внутренняя система монетизации и поддержки создателей. Покупка звёзд для канала повышает его рейтинг, видимость в рекомендациях и способствует росту аудитории!"
                ],
                "какой минимальный заказ": [
                    "Минимальная сумма заказа зависит от услуги:\n- Звёзды: от 100 рублей\n- Реклама: от 1000 рублей\n- Видео/изображения: от 1500 рублей",
                    "Минимальные суммы заказов:\n• Покупка звёзд - от 100 руб.\n• Рекламные кампании - от 1000 руб.\n• Создание контента - от 1500 руб.\n• Индивидуальные проекты - обсуждается отдельно",
                    "Минимальные заказы по услугам:\n- Звёзды: от 100 рублей\n- Реклама: от 1000 рублей\n- Видео и графика: от 1500 рублей\n- Комплексные решения: индивидуальный расчет"
                ],
                "можно ли оплатить картой": [
                    "Да, мы принимаем все основные платежные системы:\n- Банковские карты (Visa, Mastercard, Мир)\n- ЮMoney\n- Qiwi\n- Криптовалюты (по запросу)\n- Другие популярные способы",
                    "Мы принимаем различные способы оплаты:\n• Банковские карты (Visa, Mastercard, Мир)\n• Электронные кошельки (ЮMoney, Qiwi)\n• Криптовалюты (по предварительному согласованию)\n• Другие удобные для вас методы",
                    "Доступные способы оплаты:\n- Банковские карты всех основных систем\n- Популярные электронные кошельки\n- Криптовалюты (при необходимости)\n- Другие удобные варианты по запросу"
                ],
                "есть ли партнерская программа": [
                    "Да! У нас есть выгодная партнерская программа. Зарабатывайте до 20% с каждого привлеченного клиента. Подробности уточняйте у поддержки!",
                    "Конечно! У нас действует партнерская программа с комиссией до 20% от привлеченных клиентов. Для получения деталей обратитесь в поддержку!",
                    "Да, мы предлагаем партнерскую программу с вознаграждением до 20%. Для получения подробной информации свяжитесь с нашей поддержкой!"
                ],
                "как отследить статус заказа": [
                    "Статус заказа можно отследить:\n- В личном кабинете на сайте\n- Через нашего бота\n- Написав в поддержку\nМы также уведомляем о смене статуса по email.",
                    "Отслеживание статуса заказа:\n• В вашем личном кабинете на сайте\n• Через нашего Telegram-бота\n• Обратившись в поддержку\n• По email-уведомлениям при изменении статуса",
                    "Узнать статус заказа можно:\n- В разделе 'Личный кабинет' на сайте\n- Через нашего бота в Telegram\n- Написав в службу поддержки\n- По email-оповещениям при смене статуса"
                ],
                "можно ли заказать срочно": [
                    "Да, мы предоставляем услуги срочного выполнения с доплатой 30%. Уточняйте возможность срочного выполнения при оформлении заказа!",
                    "Мы предлагаем срочное выполнение заказов с дополнительной оплатой 30%. Возможность срочного выполнения уточняйте при оформлении заказа!",
                    "Да, доступно срочное выполнение с надбавкой 30% к стоимости. Наличие возможности срочного выполнения уточняйте при заказе!"
                ],
                "какие требования к контенту": [
                    "Мы работаем с любым легальным контентом, кроме:\n- Пропаганды насилия\n- Взрослого контента\n- Мошеннических схем\n- Запрещенных материалов",
                    "Принимаем любой легальный контент, за исключением:\n• Пропаганды насилия и экстремизма\n• Контента для взрослых\n• Мошеннических материалов\n• Запрещенного законодательством контента",
                    "Работаем с легальным контентам, не принимаем:\n- Материалы, пропагандирующие насилие\n- Взрослый контент\n- Мошеннические схемы\n- Запрещенные законом материалы"
                ],
                "расскажи что-нибудь интересное": [
                    "Конечно! Знаете ли вы, что Telegram был запущен в 2013 году братьями Дуровыми? Сейчас у платформы более 700 миллионов активных пользователей! Или вот еще факт: первое сообщение в Telegram было отправлено 14 августа 2013 года.",
                    "Интересный факт: создатели Telegram - братья Дуровы, также основавшие ВКонтакте. Павел Дуров известен своей приверженностью защите приватности пользователей. Telegram использует шифрование для защиты переписок!",
                    "Знаете ли вы, что Telegram стал особенно популярен благодаря своему фокусу на безопасность и приватность? Платформа использует собственный протокол шифрования MTProto и позволяет создавать 'секретные чаты' с самоуничтожающимися сообщениями!"
                ]
            },

            // Универсальные ответы для любых вопросов
            universalResponses: [
                "Отличный вопрос! На основе моего анализа, я могу сказать, что это интересная тема. Давайте обсудим её подробнее.",
                "Интересно! Я думаю над вашим вопросом... Мой искусственный интеллект обрабатывает эту информацию.",
                "Хм, вы задали сложный вопрос. Позвольте мне подумать... Да, я понял суть!",
                "Ваш вопрос требует глубокого анализа. На основе моих знаний я могу сказать следующее...",
                "Я внимательно изучил ваш вопрос. Вот что я могу сказать по этому поводу...",
                "Интересный запрос! Мой AI-мозг обрабатывает информацию... И вот мой ответ:",
                "Вы затронули важную тему. Позвольте мне поделиться своими мыслями на этот счёт...",
                "Отличный вопрос для обсуждения! На основе моих обширных знаний я могу сказать следующее...",
                "Вы задали действительно интересный вопрос. Давайте разберём его вместе!",
                "Мой искусственный интеллект проанализировал ваш запрос. Вот что я могу вам сказать..."
            ],

            // Фразы для демонстрации "мышления"
            thinkingPhrases: [
                "Анализирую ваш вопрос...",
                "Ищу лучший ответ в своей базе знаний...",
                "Обрабатываю информацию...",
                "Мой AI-мозг работает над ответом...",
                "Изучаю все аспекты вашего вопроса...",
                "Провожу глубокий анализ...",
                "Сканирую свою базу знаний...",
                "Формирую наиболее точный ответ..."
            ],

            // Получить ответ на любой вопрос
            getResponse: function(message) {
                const lowerMessage = message.toLowerCase();
                
                // Поиск точного совпадения в базе знаний
                for (const [key, responses] of Object.entries(this.knowledgeBase)) {
                    if (lowerMessage.includes(key)) {
                        // Возвращаем случайный ответ из массива вариантов
                        return responses[Math.floor(Math.random() * responses.length)];
                    }
                }
                
                // Умный поиск по ключевым словам
                const keywordResponses = {
                    "звезд": this.knowledgeBase["как купить звезды"][0],
                    "реклам": this.knowledgeBase["сколько стоит реклама"][0],
                    "заказ": this.knowledgeBase["как оформить заказ"][0],
                    "скидк": this.knowledgeBase["есть ли скидки"][0],
                    "врем": this.knowledgeBase["сколько времени выполняется заказ"][0],
                    "гарант": this.knowledgeBase["гарантии"][0],
                    "мин": this.knowledgeBase["какой минимальный заказ"][0],
                    "оплат": this.knowledgeBase["можно ли оплатить картой"][0],
                    "партнер": this.knowledgeBase["есть ли партнерская программа"][0],
                    "статус": this.knowledgeBase["как отследить статус заказа"][0],
                    "срочн": this.knowledgeBase["можно ли заказать срочно"][0],
                    "требован": this.knowledgeBase["какие требования к контенту"][0],
                    "подробн": this.knowledgeBase["расскажи о себе"][0],
                    "telegram": this.knowledgeBase["что такое telegram звезды"][0],
                    "поддержк": this.knowledgeBase["как связаться с поддержкой"][0]
                };
                
                for (const [keyword, response] of Object.entries(keywordResponses)) {
                    if (lowerMessage.includes(keyword)) {
                        return response;
                    }
                }
                
                // Если вопрос не распознан - использовать универсальный ответ
                const randomResponse = this.universalResponses[Math.floor(Math.random() * this.universalResponses.length)];
                const randomThinking = this.thinkingPhrases[Math.floor(Math.random() * this.thinkingPhrases.length)];
                
                return `${randomThinking}\n\n${randomResponse}\n\nЕсли вам нужна более конкретная информация о наших услугах, задайте вопрос более конкретно или используйте быстрые ответы выше!`;
            },

            // Получить фразу "мышления"
            getThinkingPhrase: function() {
                return this.thinkingPhrases[Math.floor(Math.random() * this.thinkingPhrases.length)];
            }
        };

        // Инициализация данных
        const initLocalStorage = () => {
            if (!localStorage.getItem('users')) {
                const adminUser = {
                    id: 1,
                    name: 'Администратор',
                    email: 'admin@st1xlox.com',
                    password: 'admin123',
                    role: 'admin',
                    status: 'active',
                    registrationDate: new Date().toISOString(),
                    bio: 'Администратор системы st1xlox Services',
                    onlineStatus: 'online',
                    avatar: null,
                    emailVerified: true
                };
                
                const secondAdmin = {
                    id: 2,
                    name: 'Модератор',
                    email: 'moderator@st1xlox.com',
                    password: 'moderator123',
                    role: 'admin',
                    status: 'active',
                    registrationDate: new Date().toISOString(),
                    bio: 'Модератор системы st1xlox Services',
                    onlineStatus: 'online',
                    avatar: null,
                    emailVerified: true
                };
                
                localStorage.setItem('users', JSON.stringify([adminUser, secondAdmin]));
            }
            if (!localStorage.getItem('currentUser')) {
                localStorage.setItem('currentUser', JSON.stringify(null));
            }
            if (!localStorage.getItem('reviews')) {
                localStorage.setItem('reviews', JSON.stringify([
                    {
                        id: 1,
                        name: "Алексей",
                        text: "Отличный сервис! Заказал звёзды для канала, всё пришло быстро и без проблем. Рекомендую!",
                        rating: 5,
                        date: "2 недели назад",
                        approved: true
                    },
                    {
                        id: 2,
                        name: "Мария",
                        text: "Быстрая и качественная работа. Заказывала рекламу, результат превзошёл ожидания. Обязательно вернусь!",
                        rating: 5,
                        date: "3 недели назад",
                        approved: true
                    },
                    {
                        id: 3,
                        name: "Дмитрий",
                        text: "Профессиональный подход, вежливая поддержка. Заказывал несколько раз, всегда доволен результатом.",
                        rating: 5,
                        date: "1 месяц назад",
                        approved: true
                    }
                ]));
            }
            if (!localStorage.getItem('orders')) {
                const sampleOrders = [
                    {
                        id: 1,
                        userId: 1,
                        type: 'video',
                        serviceType: 'promo',
                        data: { 'video-type': 'promo', 'video-style': 'anime' },
                        status: 'completed',
                        date: new Date().toLocaleDateString('ru-RU'),
                        price: 500,
                        hasReview: false
                    },
                    {
                        id: 2,
                        userId: 1,
                        type: 'images',
                        serviceType: 'post',
                        data: { 'image-type': 'post', 'image-count': '5' },
                        status: 'pending',
                        date: new Date().toLocaleDateString('ru-RU'),
                        price: 500,
                        hasReview: false
                    }
                ];
                localStorage.setItem('orders', JSON.stringify(sampleOrders));
            }
            if (!localStorage.getItem('chatMessages')) {
                const messages = [
                    {
                        id: 1,
                        username: "st1xlox AI",
                        text: "Привет! Я st1xlox AI - умный помощник. Могу ответить на любой ваш вопрос! Чем могу помочь?",
                        time: new Date().toLocaleTimeString('ru-RU', { hour: '2-digit', minute: '2-digit' }),
                        isOwn: false,
                        isAI: true,
                        isUltraAI: true
                    }
                ];
                localStorage.setItem('chatMessages', JSON.stringify(messages));
            }
            if (!localStorage.getItem('emailVerifications')) {
                localStorage.setItem('emailVerifications', JSON.stringify({}));
            }
        };

        // Управление навигацией
        const setupNavigation = () => {
            document.addEventListener('click', (e) => {
                if (e.target.matches('[data-page]') || e.target.closest('[data-page]')) {
                    e.preventDefault();
                    const target = e.target.matches('[data-page]') ? e.target : e.target.closest('[data-page]');
                    const pageId = target.getAttribute('data-page');
                    showPage(pageId);
                    
                    // Обновляем активное состояние в навигации
                    document.querySelectorAll('.nav-link').forEach(link => link.classList.remove('active'));
                    if (target.classList.contains('nav-link')) {
                        target.classList.add('active');
                    }
                }
            });
        };

        // Показать страницу
        const showPage = (pageId) => {
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active-page');
                page.classList.remove('page-transition');
            });
            const targetPage = document.getElementById(pageId);
            if (targetPage) {
                targetPage.classList.add('active-page');
                setTimeout(() => {
                    targetPage.classList.add('page-transition');
                }, 10);
                
                const currentUser = JSON.parse(localStorage.getItem('currentUser'));
                const protectedPages = ['dashboard', 'admin'];
                
                if (protectedPages.includes(pageId) && !currentUser) {
                    showNotification('Для доступа к этой странице необходимо войти в систему', 'warning');
                    showPage('login');
                    return;
                }
                
                if (pageId === 'admin' && currentUser && currentUser.role !== 'admin') {
                    showNotification('У вас нет прав доступа к этой странице', 'error');
                    showPage('dashboard');
                    return;
                }
                
                if (pageId === 'dashboard') {
                    updateDashboard();
                } else if (pageId === 'admin') {
                    updateAdminPanel();
                } else if (pageId === 'reviews') {
                    loadReviews();
                } else if (pageId === 'chat') {
                    loadAIChat();
                } else if (pageId === 'orders') {
                    setupOrderConstructor();
                } else if (pageId === 'home') {
                    setupServiceRedirects();
                } else if (pageId === 'stars') {
                    setupGalaxyStars();
                } else if (pageId === 'login' || pageId === 'register') {
                    generateCaptcha(pageId);
                }
            }
            
            window.scrollTo(0, 0);
        };

        // Генерация капчи
        const generateCaptcha = (pageId) => {
            const chars = 'ABCDEFGHJKLMNPQRSTUVWXYZabcdefghjkmnpqrstuvwxyz23456789';
            let captcha = '';
            for (let i = 0; i < 5; i++) {
                captcha += chars.charAt(Math.floor(Math.random() * chars.length));
            }
            
            const captchaElement = document.getElementById(`${pageId}-captcha-text`);
            if (captchaElement) {
                captchaElement.textContent = captcha;
            }
            
            return captcha;
        };

        // Валидация капчи
        const validateCaptcha = (pageId) => {
            const captchaInput = document.getElementById(`${pageId}-captcha-input`);
            const captchaText = document.getElementById(`${pageId}-captcha-text`);
            
            if (captchaInput && captchaText) {
                return captchaInput.value === captchaText.textContent;
            }
            return false;
        };

        // Умный редирект с главной страницы
        const setupServiceRedirects = () => {
            document.querySelectorAll('.hero-feature-card').forEach(card => {
                card.addEventListener('click', function() {
                    const service = this.getAttribute('data-service');
                    showPage('orders');
                    
                    setTimeout(() => {
                        const tab = document.querySelector(`.service-option-card[data-service="${service}"]`);
                        if (tab) {
                            tab.click();
                        }
                    }, 500);
                });
            });
        };

        // НОВАЯ ФУНКЦИЯ: Настройка интерактивного конструктора заказов
        const setupOrderConstructor = () => {
            const stepIndicators = document.querySelectorAll('.step-indicator');
            const stepContents = document.querySelectorAll('.step-content');
            const serviceOptions = document.querySelectorAll('.service-option-card');
            const nextButtons = document.querySelectorAll('.next-step');
            const prevButtons = document.querySelectorAll('.prev-step');
            const submitButton = document.getElementById('submit-order');
            
            let currentStep = 1;
            let selectedService = 'video';
            let selectedServiceType = 'promo';
            let selectedStyle = 'modern';
            let selectedOptions = [];
            let orderPrice = 500;

            // Функция для обновления отображения шагов
            const updateSteps = () => {
                stepIndicators.forEach(indicator => {
                    const step = parseInt(indicator.getAttribute('data-step'));
                    indicator.classList.remove('active', 'completed');
                    
                    if (step === currentStep) {
                        indicator.classList.add('active');
                    } else if (step < currentStep) {
                        indicator.classList.add('completed');
                    }
                });
                
                stepContents.forEach(content => {
                    const step = parseInt(content.getAttribute('data-step'));
                    content.classList.remove('active');
                    
                    if (step === currentStep) {
                        content.classList.add('active');
                    }
                });
                
                // Обновляем прогресс
                const progressPercent = ((currentStep - 1) / 3) * 100;
                document.querySelector('.progress-bar').style.width = `${progressPercent}%`;
                document.getElementById('progress-percent').textContent = `${Math.round(progressPercent)}%`;
                document.getElementById('current-step').textContent = getStepName(currentStep);
            };

            // Функция для получения названия шага
            const getStepName = (step) => {
                const stepNames = {
                    1: 'Выбор услуги',
                    2: 'Настройка',
                    3: 'Детали',
                    4: 'Подтверждение'
                };
                return stepNames[step] || 'Неизвестный шаг';
            };

            // Функция для обновления предпросмотра заказа
            const updateOrderPreview = () => {
                document.getElementById('selected-service-preview').textContent = getServiceName(selectedService);
                document.getElementById('selected-service-type-preview').textContent = getServiceTypeName(selectedService, selectedServiceType);
                document.getElementById('estimated-price').textContent = `${orderPrice} ₽`;
                
                // Обновляем финальную сводку
                document.getElementById('summary-service').textContent = getServiceName(selectedService);
                document.getElementById('summary-service-type').textContent = getServiceTypeName(selectedService, selectedServiceType);
                document.getElementById('summary-style').textContent = getStyleName(selectedStyle);
                document.getElementById('summary-options').textContent = selectedOptions.length > 0 ? selectedOptions.join(', ') : 'Нет';
                document.getElementById('summary-total').textContent = `${orderPrice} ₽`;
            };

            // Функция для расчета стоимости заказа
            const calculateOrderPrice = () => {
                let price = getServiceTypePrice(selectedService, selectedServiceType);
                
                // Доплата за срочность
                if (selectedOptions.includes('fast')) {
                    price = Math.round(price * 1.3);
                }
                
                // Доплата за приоритетную поддержку
                if (selectedOptions.includes('support')) {
                    price += 100;
                }
                
                orderPrice = price;
                return orderPrice;
            };

            // Функция для получения цены типа услуги
            const getServiceTypePrice = (service, serviceType) => {
                const prices = {
                    'video': {
                        'promo': 500,
                        'intro': 350,
                        'footage': 500
                    },
                    'images': {
                        'banner': 200,
                        'post': 100,
                        'pic': 150
                    },
                    'avatar': {
                        'anime': 100,
                        'movie': 150,
                        'complex': 250
                    },
                    'ads': {
                        '1': 350,
                        '3': 600,
                        '7': 1200,
                        '14': 2000
                    }
                };
                
                return prices[service]?.[serviceType] || 0;
            };

            // Функция для получения названия услуги
            const getServiceName = (service) => {
                const serviceNames = {
                    'video': 'Создание видео',
                    'images': 'Графический дизайн',
                    'avatar': 'Дизайн аватарки',
                    'ads': 'Реклама в Telegram'
                };
                return serviceNames[service] || 'Неизвестная услуга';
            };

            // Функция для получения названия типа услуги
            const getServiceTypeName = (service, serviceType) => {
                const serviceTypeNames = {
                    'video': {
                        'promo': 'Промо-ролик',
                        'intro': 'Интро/Аутро',
                        'footage': 'Футажи'
                    },
                    'images': {
                        'banner': 'Баннер',
                        'post': 'Пост для соц. сетей',
                        'pic': 'Пикчи'
                    },
                    'avatar': {
                        'anime': 'Аниме',
                        'movie': 'Фильм',
                        'complex': 'Сложная работа'
                    },
                    'ads': {
                        '1': '1 день',
                        '3': '3 дня',
                        '7': '7 дней',
                        '14': '14 дней'
                    }
                };
                
                return serviceTypeNames[service]?.[serviceType] || 'Неизвестный тип';
            };

            // Функция для получения названия стиля
            const getStyleName = (style) => {
                const styleNames = {
                    'modern': 'Современный',
                    'minimal': 'Минимализм',
                    'luxury': 'Премиум'
                };
                return styleNames[style] || 'Неизвестный стиль';
            };

            // Функция для обновления деталей заказа в зависимости от выбранной услуги
            const updateOrderDetails = () => {
                const orderDetailsForm = document.getElementById('order-details-form');
                
                // Очищаем форму
                orderDetailsForm.innerHTML = '';
                
                // Добавляем общие поля
                const commonFields = `
                    <div class="mb-3">
                        <label for="order-title" class="form-label">Название проекта</label>
                        <input type="text" class="form-control" id="order-title" placeholder="${getProjectTitlePlaceholder(selectedService)}" required>
                    </div>
                    <div class="mb-3">
                        <label for="order-description" class="form-label">Описание проекта</label>
                        <textarea class="form-control" id="order-description" rows="4" placeholder="${getProjectDescriptionPlaceholder(selectedService)}" required></textarea>
                    </div>
                `;
                
                orderDetailsForm.innerHTML = commonFields;
                
                // Добавляем специфические поля для каждой услуги
                switch(selectedService) {
                    case 'video':
                        orderDetailsForm.innerHTML += `
                            <div class="mb-3">
                                <label for="video-type" class="form-label">Тип видео</label>
                                <select class="form-select" id="video-type" required>
                                    <option value="">Выберите тип видео</option>
                                    <option value="promo" data-price="500">Промо-ролик (500 ₽)</option>
                                    <option value="intro" data-price="350">Интро/Аутро (350 ₽)</option>
                                    <option value="footage" data-price="500">Футажи (500 ₽)</option>
                                </select>
                            </div>
                            <div class="mb-3">
                                <label for="video-duration" class="form-label">Продолжительность (секунды)</label>
                                <input type="number" class="form-control" id="video-duration" min="5" max="300" value="30">
                            </div>
                        `;
                        break;
                    case 'images':
                        orderDetailsForm.innerHTML += `
                            <div class="mb-3">
                                <label for="image-type" class="form-label">Тип изображения</label>
                                <select class="form-select" id="image-type" required>
                                    <option value="">Выберите тип изображения</option>
                                    <option value="banner" data-price="200">Баннер (200 ₽)</option>
                                    <option value="post" data-price="100">Пост для соц. сетей (100 ₽)</option>
                                    <option value="pic" data-price="150">Пикчи (150 ₽)</option>
                                </select>
                            </div>
                            <div class="mb-3">
                                <label for="image-count" class="form-label">Количество изображений</label>
                                <input type="number" class="form-control" id="image-count" min="1" max="10" value="1">
                            </div>
                        `;
                        break;
                    case 'avatar':
                        orderDetailsForm.innerHTML += `
                            <div class="mb-3">
                                <label for="avatar-style" class="form-label">Стиль аватарки</label>
                                <select class="form-select" id="avatar-style" required>
                                    <option value="">Выберите стиль</option>
                                    <option value="anime" data-price="100">Аниме (100 ₽)</option>
                                    <option value="movie" data-price="150">Фильм (150 ₽)</option>
                                    <option value="complex" data-price="250">Сложная работа (250 ₽)</option>
                                </select>
                            </div>
                            <div class="mb-3">
                                <label for="avatar-reference" class="form-label">Описание или референс</label>
                                <textarea class="form-control" id="avatar-reference" rows="3" placeholder="Опишите, как должна выглядеть ваша аватарка..."></textarea>
                            </div>
                        `;
                        break;
                    case 'ads':
                        orderDetailsForm.innerHTML += `
                            <div class="mb-3">
                                <label for="ad-duration" class="form-label">Продолжительность рекламы</label>
                                <select class="form-select" id="ad-duration" required>
                                    <option value="">Выберите продолжительность</option>
                                    <option value="1" data-price="350">1 день (350 ₽)</option>
                                    <option value="3" data-price="600">3 дня (600 ₽)</option>
                                    <option value="7" data-price="1200">7 дней (1200 ₽)</option>
                                    <option value="14" data-price="2000">14 дней (2000 ₽)</option>
                                </select>
                            </div>
                            <div class="mb-3">
                                <label for="ad-text" class="form-label">Текст рекламы</label>
                                <textarea class="form-control" id="ad-text" rows="3" placeholder="Введите текст для рекламного поста..."></textarea>
                            </div>
                        `;
                        break;
                }
                
                // Добавляем обработчики для обновления цены при изменении типа услуги
                const serviceSpecificSelects = orderDetailsForm.querySelectorAll('select');
                serviceSpecificSelects.forEach(select => {
                    select.addEventListener('change', function() {
                        const selectedOption = this.options[this.selectedIndex];
                        selectedServiceType = this.value;
                        calculateOrderPrice();
                        updateOrderPreview();
                    });
                });

                // Устанавливаем значение по умолчанию для выпадающего списка
                if (serviceSpecificSelects.length > 0) {
                    serviceSpecificSelects[0].selectedIndex = 0;
                    selectedServiceType = serviceSpecificSelects[0].value;
                }
            };

            // Функция для получения заголовка проекта в зависимости от услуги
            const getProjectTitlePlaceholder = (service) => {
                const titles = {
                    'video': 'Мой промо-ролик',
                    'images': 'Мой дизайн-проект',
                    'avatar': 'Моя уникальная аватарка',
                    'ads': 'Рекламная кампания'
                };
                return titles[service] || 'Мой крутой проект';
            };

            // Функция для получения описания проекта в зависимости от услуги
            const getProjectDescriptionPlaceholder = (service) => {
                const descriptions = {
                    'video': 'Опишите концепцию вашего видео, желаемый стиль и ключевые моменты...',
                    'images': 'Опишите идею для дизайна, цветовую гамму и основные элементы...',
                    'avatar': 'Опишите желаемый стиль аватарки, характер и предпочтения...',
                    'ads': 'Опишите целевую аудиторию, ключевое сообщение и цели рекламы...'
                };
                return descriptions[service] || 'Опишите ваши пожелания и требования...';
            };

            // Обработчики для выбора услуги
            serviceOptions.forEach(option => {
                option.addEventListener('click', function() {
                    serviceOptions.forEach(opt => opt.classList.remove('active'));
                    this.classList.add('active');
                    selectedService = this.getAttribute('data-service');
                    selectedServiceType = 'promo'; // Сброс к значению по умолчанию
                    calculateOrderPrice();
                    updateOrderPreview();
                    updateOrderDetails();
                });
            });

            // Обработчики для дополнительных опций
            document.querySelectorAll('input[type="checkbox"]').forEach(checkbox => {
                checkbox.addEventListener('change', function() {
                    if (this.checked) {
                        if (!selectedOptions.includes(this.id.replace('option-', ''))) {
                            selectedOptions.push(this.id.replace('option-', ''));
                        }
                    } else {
                        const index = selectedOptions.indexOf(this.id.replace('option-', ''));
                        if (index > -1) {
                            selectedOptions.splice(index, 1);
                        }
                    }
                    calculateOrderPrice();
                    updateOrderPreview();
                });
            });

            // Обработчики для выбора стиля
            document.querySelectorAll('input[name="style"]').forEach(radio => {
                radio.addEventListener('change', function() {
                    selectedStyle = this.id.replace('style-', '');
                    updateOrderPreview();
                });
            });

            // Обработчики для кнопок навигации
            nextButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const nextStep = parseInt(this.getAttribute('data-next'));
                    if (nextStep > currentStep) {
                        currentStep = nextStep;
                        updateSteps();
                        updateOrderPreview();
                    }
                });
            });

            prevButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const prevStep = parseInt(this.getAttribute('data-prev'));
                    if (prevStep < currentStep) {
                        currentStep = prevStep;
                        updateSteps();
                        updateOrderPreview();
                    }
                });
            });

            // Обработчик для отправки заказа
            if (submitButton) {
                submitButton.addEventListener('click', function() {
                    const agreeTerms = document.getElementById('agree-terms');
                    
                    if (!agreeTerms.checked) {
                        showNotification('Пожалуйста, согласитесь с условиями предоставления услуг', 'warning');
                        return;
                    }
                    
                    const currentUser = JSON.parse(localStorage.getItem('currentUser'));
                    if (!currentUser) {
                        showNotification('Для оформления заказа необходимо войти в систему', 'warning');
                        showPage('login');
                        return;
                    }
                    
                    const orderData = {
                        service: selectedService,
                        serviceType: selectedServiceType,
                        style: selectedStyle,
                        options: selectedOptions,
                        title: document.getElementById('order-title').value,
                        description: document.getElementById('order-description').value,
                        price: orderPrice
                    };
                    
                    // Добавляем специфические данные для каждой услуги
                    switch(selectedService) {
                        case 'video':
                            orderData.videoType = document.getElementById('video-type').value;
                            orderData.videoDuration = document.getElementById('video-duration').value;
                            break;
                        case 'images':
                            orderData.imageType = document.getElementById('image-type').value;
                            orderData.imageCount = document.getElementById('image-count').value;
                            break;
                        case 'avatar':
                            orderData.avatarStyle = document.getElementById('avatar-style').value;
                            orderData.avatarReference = document.getElementById('avatar-reference').value;
                            break;
                        case 'ads':
                            orderData.adDuration = document.getElementById('ad-duration').value;
                            orderData.adText = document.getElementById('ad-text').value;
                            break;
                    }
                    
                    const orders = JSON.parse(localStorage.getItem('orders')) || [];
                    const newOrder = {
                        id: orders.length + 1,
                        userId: currentUser.id,
                        type: selectedService,
                        serviceType: selectedServiceType,
                        data: orderData,
                        status: 'pending',
                        date: new Date().toLocaleDateString('ru-RU'),
                        price: orderPrice,
                        hasReview: false
                    };
                    
                    orders.push(newOrder);
                    localStorage.setItem('orders', JSON.stringify(orders));
                    
                    let message = `Новый заказ: ${getServiceName(selectedService)}\n\n`;
                    message += `Тип: ${getServiceTypeName(selectedService, selectedServiceType)}\n`;
                    message += `Стиль: ${getStyleName(selectedStyle)}\n`;
                    message += `Описание: ${orderData.description}\n\n`;
                    message += `Пользователь: ${currentUser.name} (${currentUser.email})`;
                    
                    const encodedMessage = encodeURIComponent(message);
                    window.open(`https://t.me/st1xloxServices_bot?text=${encodedMessage}`, '_blank');
                    
                    showNotification('Заказ оформлен! Открывается Telegram для отправки', 'success');
                    
                    // Сброс формы
                    setTimeout(() => {
                        currentStep = 1;
                        updateSteps();
                        document.getElementById('order-details-form').reset();
                        serviceOptions.forEach(opt => opt.classList.remove('active'));
                        document.querySelector('.service-option-card[data-service="video"]').classList.add('active');
                        selectedService = 'video';
                        selectedServiceType = 'promo';
                        selectedOptions = [];
                        calculateOrderPrice();
                        updateOrderPreview();
                        updateOrderDetails();
                    }, 2000);
                });
            }

            // Инициализация
            updateSteps();
            updateOrderPreview();
            updateOrderDetails();
            calculateOrderPrice();
        };

        // НОВАЯ ФУНКЦИЯ: Настройка страницы Galaxy Stars & Premium
        const setupGalaxyStars = () => {
            // Добавляем обработчики для кнопок карусели отзывов
            const carouselInner = document.getElementById('reviews-carousel-inner');
            const carouselPrev = document.getElementById('carousel-prev');
            const carouselNext = document.getElementById('carousel-next');
            
            if (carouselPrev && carouselNext) {
                carouselPrev.addEventListener('click', () => {
                    carouselInner.scrollBy({ left: -370, behavior: 'smooth' });
                });
                
                carouselNext.addEventListener('click', () => {
                    carouselInner.scrollBy({ left: 370, behavior: 'smooth' });
                });
            }
            
            // Обработчик для кнопки "Эксклюзивный доступ к премиум функциям"
            const premiumBtn = document.getElementById('premium-features-btn');
            if (premiumBtn) {
                premiumBtn.addEventListener('click', () => {
                    const premiumSteps = document.getElementById('premium-steps');
                    if (premiumSteps) {
                        premiumSteps.scrollIntoView({ behavior: 'smooth' });
                        premiumSteps.classList.add('highlight-section');
                        setTimeout(() => {
                            premiumSteps.classList.remove('highlight-section');
                        }, 2000);
                    }
                });
            }

            // Обработчик для sticky кнопки
            const stickyBtn = document.getElementById('sticky-galaxy-btn');
            if (stickyBtn) {
                stickyBtn.addEventListener('click', () => {
                    showPage('stars');
                });
            }
        };

        // НОВАЯ ФУНКЦИЯ: Загрузка AI чата
        const loadAIChat = () => {
            const chatBody = document.getElementById('ai-chat-body');
            const chatInput = document.getElementById('ai-chat-input');
            const sendBtn = document.getElementById('ai-send-btn');
            const quickReplies = document.getElementById('ai-quick-replies');

            // Очистка чата (кроме первого сообщения)
            while (chatBody.children.length > 1) {
                chatBody.removeChild(chatBody.lastChild);
            }

            // Обработчик отправки сообщения
            const sendMessage = () => {
                const message = chatInput.value.trim();
                if (!message) return;

                // Добавляем сообщение пользователя
                addMessage(message, 'user');
                chatInput.value = '';

                // Показываем индикатор набора
                const typingIndicator = document.createElement('div');
                typingIndicator.className = 'ai-typing';
                typingIndicator.innerHTML = `
                    <div class="typing-dot"></div>
                    <div class="typing-dot"></div>
                    <div class="typing-dot"></div>
                `;
                chatBody.appendChild(typingIndicator);
                chatBody.scrollTop = chatBody.scrollHeight;

                // Имитируем задержку ответа AI
                setTimeout(() => {
                    typingIndicator.remove();
                    
                    // Получаем ответ от AI
                    const aiResponse = ultraAI.getResponse(message);
                    addMessage(aiResponse, 'bot');
                }, 1000 + Math.random() * 2000);
            };

            // Функция добавления сообщения
            const addMessage = (text, sender) => {
                const messageElement = document.createElement('div');
                messageElement.className = `ai-message ${sender}`;
                messageElement.textContent = text;
                chatBody.appendChild(messageElement);
                chatBody.scrollTop = chatBody.scrollHeight;
            };

            // Обработчики событий
            sendBtn.addEventListener('click', sendMessage);
            chatInput.addEventListener('keypress', (e) => {
                if (e.key === 'Enter') {
                    sendMessage();
                }
            });

            // Обработчики быстрых ответов
            quickReplies.querySelectorAll('.quick-reply-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    const message = btn.getAttribute('data-message');
                    chatInput.value = message;
                    sendMessage();
                });
            });
        };

        // Обновление панели управления
        const updateDashboard = () => {
            const currentUser = JSON.parse(localStorage.getItem('currentUser'));
            if (currentUser) {
                // Обновляем приветствие
                document.getElementById('dashboard-welcome').textContent = `Добро пожаловать, ${currentUser.name}!`;
                
                // Обновляем дату
                const now = new Date();
                const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
                document.getElementById('current-date').textContent = now.toLocaleDateString('ru-RU', options);
                
                // Обновляем аватар
                const avatarElement = document.getElementById('profile-avatar-large');
                const dashboardAvatar = document.getElementById('dashboard-user-avatar');
                
                if (currentUser.avatar) {
                    avatarElement.innerHTML = `<img src="${currentUser.avatar}" alt="Аватар">`;
                    dashboardAvatar.innerHTML = `<img src="${currentUser.avatar}" alt="Аватар">`;
                } else {
                    avatarElement.innerHTML = `<span>${currentUser.name.charAt(0).toUpperCase()}</span>`;
                    dashboardAvatar.innerHTML = `<span>${currentUser.name.charAt(0).toUpperCase()}</span>`;
                }
                
                // Обновляем информацию о пользователе
                document.getElementById('profile-name').textContent = currentUser.name;
                document.getElementById('profile-email').textContent = currentUser.email;
                
                if (currentUser.registrationDate) {
                    const regDate = new Date(currentUser.registrationDate);
                    const formattedDate = regDate.toLocaleDateString('ru-RU');
                    document.getElementById('profile-registration-date').textContent = `Зарегистрирован: ${formattedDate}`;
                }
                
                updateUserStats(currentUser.id);
                loadOrderHistory(currentUser.id);
            }
        };

        // Обновление статистики пользователя
        const updateUserStats = (userId) => {
            const orders = JSON.parse(localStorage.getItem('orders')) || [];
            const reviews = JSON.parse(localStorage.getItem('reviews')) || [];
            
            const userOrders = orders.filter(order => order.userId === userId);
            const userReviews = reviews.filter(review => review.name === currentUser.name);
            const completedOrders = userOrders.filter(order => order.status === 'completed').length;
            const totalSpent = userOrders.reduce((sum, order) => sum + (order.price || 0), 0);
            
            // Обновляем статистику
            document.getElementById('dashboard-orders-count').textContent = userOrders.length;
            document.getElementById('dashboard-completed-orders').textContent = completedOrders;
            document.getElementById('dashboard-reviews-count').textContent = userReviews.length;
            document.getElementById('dashboard-total-spent').textContent = `${totalSpent} ₽`;
        };

        // Загрузка истории заказов
        const loadOrderHistory = (userId) => {
            const orders = JSON.parse(localStorage.getItem('orders')) || [];
            const userOrders = orders.filter(order => order.userId === userId);
            const ordersList = document.getElementById('orders-list');
            
            if (userOrders.length === 0) {
                ordersList.innerHTML = '<p class="text-center text-muted">У вас пока нет заказов</p>';
                return;
            }
            
            ordersList.innerHTML = '';
            userOrders.forEach(order => {
                const orderElement = document.createElement('div');
                orderElement.className = 'order-card';
                
                let reviewButton = '';
                if (order.status === 'completed' && !order.hasReview) {
                    reviewButton = `<button class="order-action-btn review leave-review-btn" data-order-id="${order.id}">Оставить отзыв</button>`;
                }
                
                orderElement.innerHTML = `
                    <div class="order-header">
                        <div class="order-title">Заказ #${order.id}</div>
                        <div class="order-status ${order.status}">${order.status === 'completed' ? 'Выполнен' : 'В обработке'}</div>
                    </div>
                    <div class="order-details">
                        <div class="order-detail">
                            <span class="order-detail-label">Тип:</span>
                            <span>${getOrderTypeName(order.type)}</span>
                        </div>
                        <div class="order-detail">
                            <span class="order-detail-label">Дата:</span>
                            <span>${order.date}</span>
                        </div>
                        <div class="order-detail">
                            <span class="order-detail-label">Стоимость:</span>
                            <span>${order.price || 'Не указана'} руб.</span>
                        </div>
                    </div>
                    <div class="order-actions">
                        <button class="order-action-btn view-order-btn" data-order-id="${order.id}">Подробнее</button>
                        ${reviewButton}
                    </div>
                `;
                ordersList.appendChild(orderElement);
            });
            
            // Добавляем обработчики для кнопок отзывов
            document.querySelectorAll('.leave-review-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const orderId = this.getAttribute('data-order-id');
                    openOrderReviewModal(orderId);
                });
            });

            // Добавляем обработчики для кнопок "Подробнее"
            document.querySelectorAll('.view-order-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const orderId = this.getAttribute('data-order-id');
                    viewOrderDetails(orderId);
                });
            });
        };

        // Просмотр деталей заказа
        const viewOrderDetails = (orderId) => {
            const orders = JSON.parse(localStorage.getItem('orders')) || [];
            const order = orders.find(o => o.id === parseInt(orderId));
            
            if (!order) {
                showNotification('Заказ не найден', 'error');
                return;
            }
            
            const orderDetailsHtml = `
                <div class="modal fade" id="orderDetailsModal" tabindex="-1" aria-hidden="true">
                    <div class="modal-dialog modal-dialog-centered modal-lg">
                        <div class="modal-content glass-card">
                            <div class="modal-header">
                                <h5 class="modal-title">Детали заказа #${order.id}</h5>
                                <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                            </div>
                            <div class="modal-body">
                                <div class="row">
                                    <div class="col-md-6">
                                        <p><strong>Тип услуги:</strong> ${getOrderTypeName(order.type)}</p>
                                        <p><strong>Тип заказа:</strong> ${getServiceTypeName(order.type, order.serviceType)}</p>
                                        <p><strong>Дата:</strong> ${order.date}</p>
                                        <p><strong>Статус:</strong> ${order.status === 'completed' ? 'Выполнен' : 'В обработке'}</p>
                                    </div>
                                    <div class="col-md-6">
                                        <p><strong>Стоимость:</strong> ${order.price || 0} руб.</p>
                                        <p><strong>Отзыв оставлен:</strong> ${order.hasReview ? 'Да' : 'Нет'}</p>
                                    </div>
                                </div>
                                <div class="mt-3">
                                    <h6>Описание проекта:</h6>
                                    <div class="p-3 bg-dark rounded">
                                        ${order.data.description || 'Описание отсутствует'}
                                    </div>
                                </div>
                                ${order.status === 'completed' ? `
                                <div class="mt-3">
                                    <h6>Результат:</h6>
                                    <div class="text-center">
                                        <button class="btn btn-primary" onclick="downloadOrderResult(${order.id})">
                                            <i class="fas fa-download me-2"></i>Скачать результат
                                        </button>
                                    </div>
                                </div>
                                ` : ''}
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Закрыть</button>
                            </div>
                        </div>
                    </div>
                </div>
            `;
            
            // Добавляем модальное окно в DOM
            document.body.insertAdjacentHTML('beforeend', orderDetailsHtml);
            
            // Показываем модальное окно
            const modal = new bootstrap.Modal(document.getElementById('orderDetailsModal'));
            modal.show();
            
            // Удаляем модальное окно при закрытии
            document.getElementById('orderDetailsModal').addEventListener('hidden.bs.modal', () => {
                document.getElementById('orderDetailsModal').remove();
            });
        };

        // Функция для скачивания результата заказа
        window.downloadOrderResult = (orderId) => {
            showNotification('Функция скачивания в разработке', 'info');
        };

        // Открытие модального окна для отзыва о заказе
        const openOrderReviewModal = (orderId) => {
            document.getElementById('review-order-id').value = orderId;
            document.getElementById('review-order-text').value = '';
            document.getElementById('review-order-rating').value = 0;
            
            const stars = document.querySelectorAll('#order-review-form .star');
            stars.forEach(star => {
                star.classList.remove('active', 'hover');
            });
            
            const modal = new bootstrap.Modal(document.getElementById('orderReviewModal'));
            modal.show();
        };

        // Получение названия типа заказа
        const getOrderTypeName = (type) => {
            const typeNames = {
                'video': 'Видео',
                'images': 'Изображения',
                'avatar': 'Аватарка',
                'ads': 'Реклама'
            };
            return typeNames[type] || type;
        };

        // Улучшенная админ-панель
        const updateAdminPanel = () => {
            const users = JSON.parse(localStorage.getItem('users')) || [];
            const orders = JSON.parse(localStorage.getItem('orders')) || [];
            const reviews = JSON.parse(localStorage.getItem('reviews')) || [];
            
            // Обновление статистики
            document.getElementById('admin-total-users').textContent = users.length;
            document.getElementById('admin-total-orders').textContent = orders.length;
            document.getElementById('admin-active-orders').textContent = orders.filter(order => order.status === 'pending').length;
            
            const totalRevenue = orders
                .filter(order => order.status === 'completed')
                .reduce((sum, order) => sum + (order.price || 0), 0);
            document.getElementById('admin-total-revenue').textContent = `${totalRevenue} руб.`;
            
            // Расчет дохода за текущий месяц (упрощенный)
            const currentMonthRevenue = totalRevenue * 0.3; // Пример расчета
            document.getElementById('admin-month-revenue').textContent = `${currentMonthRevenue} руб.`;
            
            document.getElementById('admin-total-reviews').textContent = reviews.length;
            document.getElementById('admin-pending-reviews').textContent = reviews.filter(review => !review.approved).length;
            
            // Обновление таблицы пользователей
            const usersTable = document.getElementById('users-table');
            usersTable.innerHTML = '';
            
            users.forEach(user => {
                const row = document.createElement('tr');
                let regDate = 'Не указана';
                if (user.registrationDate) {
                    const date = new Date(user.registrationDate);
                    regDate = date.toLocaleDateString('ru-RU');
                }
                
                row.innerHTML = `
                    <td>${user.id}</td>
                    <td>${user.name}</td>
                    <td>${user.email}</td>
                    <td><span class="badge ${user.role === 'admin' ? 'bg-danger' : 'bg-primary'}">${user.role === 'admin' ? 'Админ' : 'Пользователь'}</span></td>
                    <td>${regDate}</td>
                    <td><span class="badge ${user.status === 'active' ? 'bg-success' : 'bg-warning'}">${user.status === 'active' ? 'Активный' : 'Неактивный'}</span></td>
                    <td>
                        <button class="btn btn-sm btn-primary" onclick="editUser(${user.id})">Редактировать</button>
                        <button class="btn btn-sm btn-accent" onclick="toggleUserStatus(${user.id})">${user.status === 'active' ? 'Заблокировать' : 'Активировать'}</button>
                    </td>
                `;
                usersTable.appendChild(row);
            });
            
            // Обновление таблицы заказов
            const ordersTable = document.getElementById('orders-table');
            ordersTable.innerHTML = '';
            
            orders.forEach(order => {
                const user = users.find(u => u.id === order.userId);
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${order.id}</td>
                    <td>${user ? user.name : 'Неизвестно'}</td>
                    <td>${getOrderTypeName(order.type)}</td>
                    <td>${order.date}</td>
                    <td>${order.price || 0} руб.</td>
                    <td><span class="badge ${order.status === 'completed' ? 'bg-success' : order.status === 'pending' ? 'bg-warning' : 'bg-secondary'}">${order.status === 'completed' ? 'Выполнен' : order.status === 'pending' ? 'В обработке' : 'Отменен'}</span></td>
                    <td>
                        <button class="btn btn-sm btn-primary" onclick="viewOrder(${order.id})">Просмотр</button>
                        <button class="btn btn-sm btn-success" onclick="completeOrder(${order.id})">Завершить</button>
                        <button class="btn btn-sm btn-danger" onclick="cancelOrder(${order.id})">Отменить</button>
                    </td>
                `;
                ordersTable.appendChild(row);
            });
            
            // Обновление таблицы отзывов
            const reviewsTable = document.getElementById('reviews-table');
            reviewsTable.innerHTML = '';
            
            reviews.forEach(review => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${review.id}</td>
                    <td>${review.name}</td>
                    <td class="text-truncate" style="max-width: 200px;" title="${review.text}">${review.text}</td>
                    <td>${'★'.repeat(review.rating)}${'☆'.repeat(5-review.rating)}</td>
                    <td>${review.date}</td>
                    <td><span class="badge ${review.approved ? 'bg-success' : 'bg-warning'}">${review.approved ? 'Одобрен' : 'На модерации'}</span></td>
                    <td>
                        <button class="btn btn-sm btn-primary" onclick="approveReview(${review.id})">${review.approved ? 'Снять' : 'Одобрить'}</button>
                        <button class="btn btn-sm btn-danger" onclick="deleteReview(${review.id})">Удалить</button>
                    </td>
                `;
                reviewsTable.appendChild(row);
            });
        };

        // Загрузка отзывов в карусель
        const loadReviews = () => {
            const reviews = JSON.parse(localStorage.getItem('reviews')) || [];
            const reviewsContainer = document.getElementById('reviews-carousel-inner');
            
            reviewsContainer.innerHTML = '';
            
            if (reviews.length === 0) {
                reviewsContainer.innerHTML = `
                    <div class="review-carousel-item">
                        <div class="text-center">
                            <p class="text-muted">Пока нет отзывов.</p>
                        </div>
                    </div>
                `;
                return;
            }
            
            const approvedReviews = reviews.filter(review => review.approved);
            
            if (approvedReviews.length === 0) {
                reviewsContainer.innerHTML = `
                    <div class="review-carousel-item">
                        <div class="text-center">
                            <p class="text-muted">Отзывы на модерации. Скоро они появятся здесь!</p>
                        </div>
                    </div>
                `;
                return;
            }
            
            approvedReviews.forEach((review) => {
                const reviewElement = document.createElement('div');
                reviewElement.className = 'review-carousel-item';
                reviewElement.innerHTML = `
                    <div class="review-header">
                        <div class="review-avatar">${review.name.charAt(0)}</div>
                        <div class="review-author-info">
                            <div class="review-author-name">${review.name}</div>
                            <div class="review-date">${review.date}</div>
                        </div>
                    </div>
                    <div class="review-rating-stars">
                        ${Array.from({length: 5}, (_, i) => 
                            `<i class="fas fa-star ${i < review.rating ? 'text-warning' : 'text-secondary'}"></i>`
                        ).join('')}
                    </div>
                    <div class="review-text-modern">${review.text}</div>
                    <div class="review-quote">"</div>
                `;
                reviewsContainer.appendChild(reviewElement);
            });
        };

        // Система аутентификации с подтверждением email
        const setupAuth = () => {
            // Форма входа
            document.getElementById('login-form').addEventListener('submit', (e) => {
                e.preventDefault();
                
                // Валидация капчи
                if (!validateCaptcha('login')) {
                    showNotification('Неверный код подтверждения', 'error');
                    generateCaptcha('login');
                    return;
                }
                
                const email = document.getElementById('login-email').value;
                const password = document.getElementById('login-password').value;
                
                const users = JSON.parse(localStorage.getItem('users')) || [];
                const user = users.find(u => u.email === email && u.password === password);
                
                if (user) {
                    localStorage.setItem('currentUser', JSON.stringify(user));
                    updateNavigation();
                    showNotification('Успешный вход в систему!', 'success');
                    showPage('home');
                } else {
                    showNotification('Неверный email или пароль', 'error');
                    generateCaptcha('login');
                }
            });
            
            // Форма регистрации
            document.getElementById('register-form').addEventListener('submit', (e) => {
                e.preventDefault();
                
                // Валидация капчи
                if (!validateCaptcha('register')) {
                    showNotification('Неверный код подтверждения', 'error');
                    generateCaptcha('register');
                    return;
                }
                
                const name = document.getElementById('register-name').value;
                const email = document.getElementById('register-email').value;
                const password = document.getElementById('register-password').value;
                const confirmPassword = document.getElementById('register-confirm-password').value;
                
                if (password !== confirmPassword) {
                    showNotification('Пароли не совпадают', 'error');
                    return;
                }
                
                const users = JSON.parse(localStorage.getItem('users')) || [];
                const existingUser = users.find(u => u.email === email);
                
                if (existingUser) {
                    showNotification('Пользователь с таким email уже существует', 'error');
                    return;
                }
                
                const newUser = {
                    id: users.length + 1,
                    name,
                    email,
                    password,
                    role: 'user',
                    status: 'active',
                    registrationDate: new Date().toISOString(),
                    bio: '',
                    onlineStatus: 'online',
                    avatar: null,
                    emailVerified: true
                };
                
                users.push(newUser);
                localStorage.setItem('users', JSON.stringify(users));
                localStorage.setItem('currentUser', JSON.stringify(newUser));
                updateNavigation();
                showNotification('Регистрация прошла успешно!', 'success');
                showPage('home');
            });
            
            // Кнопка выхода
            document.getElementById('logout-btn').addEventListener('click', (e) => {
                e.preventDefault();
                localStorage.setItem('currentUser', JSON.stringify(null));
                updateNavigation();
                showNotification('Вы вышли из системы', 'info');
                showPage('home');
            });
            
            // Настройка загрузки аватара
            setupAvatarUpload();
            
            updateNavigation();
        };

        // Настройка загрузки аватара
        const setupAvatarUpload = () => {
            const avatarUploadZone = document.getElementById('avatar-upload-zone');
            const avatarFileInput = document.getElementById('avatar-file-input');
            const avatarPreview = document.getElementById('avatar-preview-modal');
            const avatarSaveBtn = document.getElementById('avatar-save-btn');
            
            // Обработчик клика по зоне загрузки
            avatarUploadZone.addEventListener('click', () => {
                avatarFileInput.click();
            });
            
            // Обработчик перетаскивания файлов
            avatarUploadZone.addEventListener('dragover', (e) => {
                e.preventDefault();
                avatarUploadZone.style.borderColor = 'var(--neon-pink)';
                avatarUploadZone.style.background = 'rgba(179, 103, 255, 0.1)';
            });
            
            avatarUploadZone.addEventListener('dragleave', () => {
                avatarUploadZone.style.borderColor = 'var(--neon-purple)';
                avatarUploadZone.style.background = '';
            });
            
            avatarUploadZone.addEventListener('drop', (e) => {
                e.preventDefault();
                avatarUploadZone.style.borderColor = 'var(--neon-purple)';
                avatarUploadZone.style.background = '';
                
                if (e.dataTransfer.files.length > 0) {
                    handleAvatarFile(e.dataTransfer.files[0]);
                }
            });
            
            // Обработчик выбора файла через диалог
            avatarFileInput.addEventListener('change', (e) => {
                if (e.target.files.length > 0) {
                    handleAvatarFile(e.target.files[0]);
                }
            });
            
            // Обработчик сохранения аватара
            avatarSaveBtn.addEventListener('click', () => {
                const currentUser = JSON.parse(localStorage.getItem('currentUser'));
                if (currentUser) {
                    const users = JSON.parse(localStorage.getItem('users'));
                    const userIndex = users.findIndex(u => u.id === currentUser.id);
                    
                    if (userIndex !== -1) {
                        const avatarUrl = avatarPreview.querySelector('img')?.src;
                        if (avatarUrl) {
                            users[userIndex].avatar = avatarUrl;
                            localStorage.setItem('users', JSON.stringify(users));
                            localStorage.setItem('currentUser', JSON.stringify(users[userIndex]));
                            
                            // Обновляем аватар в интерфейсе
                            updateNavigation();
                            updateDashboard();
                            
                            // Закрываем модальное окно
                            const modal = bootstrap.Modal.getInstance(document.getElementById('avatarUploadModal'));
                            modal.hide();
                            
                            showNotification('Аватар успешно обновлен!', 'success');
                        }
                    }
                }
            });
            
            // Функция обработки файла аватарки
            const handleAvatarFile = (file) => {
                // Проверка типа файла
                const validTypes = ['image/jpeg', 'image/jpg', 'image/png', 'image/gif'];
                if (!validTypes.includes(file.type)) {
                    showNotification('Пожалуйста, выберите изображение в формате JPG, PNG или GIF', 'error');
                    return;
                }
                
                // Проверка размера файла (максимум 5MB)
                const maxSize = 5 * 1024 * 1024; // 5MB в байтах
                if (file.size > maxSize) {
                    showNotification('Размер файла не должен превышать 5MB', 'error');
                    return;
                }
                
                // Создание предпросмотра
                const reader = new FileReader();
                reader.onload = function(e) {
                    const avatarUrl = e.target.result;
                    
                    // Показываем предпросмотр
                    avatarPreview.innerHTML = `<img src="${avatarUrl}" alt="Предпросмотр аватара">`;
                    
                    // Показываем элементы для редактирования
                    document.getElementById('avatar-crop-controls').classList.remove('d-none');
                };
                reader.readAsDataURL(file);
            };
        };

        // Обновление навигации
        const updateNavigation = () => {
            const currentUser = JSON.parse(localStorage.getItem('currentUser'));
            const authNav = document.getElementById('auth-nav');
            const userNav = document.getElementById('user-nav');
            const adminBadge = document.getElementById('admin-badge');
            
            if (currentUser) {
                authNav.classList.add('d-none');
                userNav.classList.remove('d-none');
                document.getElementById('username-display').textContent = currentUser.name;
                
                const userAvatar = document.getElementById('user-avatar');
                if (currentUser.avatar) {
                    userAvatar.innerHTML = `<img src="${currentUser.avatar}" alt="Аватар">`;
                } else {
                    userAvatar.innerHTML = `<span>${currentUser.name.charAt(0).toUpperCase()}</span>`;
                }
                
                if (currentUser.role === 'admin') {
                    adminBadge.classList.remove('d-none');
                } else {
                    adminBadge.classList.add('d-none');
                }
                
                const adminLinks = document.querySelectorAll('.admin-only');
                if (currentUser.role === 'admin') {
                    adminLinks.forEach(link => link.classList.remove('d-none'));
                } else {
                    adminLinks.forEach(link => link.classList.add('d-none'));
                }
            } else {
                authNav.classList.remove('d-none');
                userNav.classList.add('d-none');
            }
        };

        // Система заказов
        const setupOrders = () => {
            // Форма связи с администрацией
            document.getElementById('contact-form')?.addEventListener('submit', (e) => {
                e.preventDefault();
                const email = document.getElementById('contact-email').value;
                const telegram = document.getElementById('contact-telegram').value;
                const message = document.getElementById('contact-message').value;
                
                const fullMessage = `Email: ${email}\nTelegram: @${telegram}\nСообщение: ${message}`;
                const encodedMessage = encodeURIComponent(fullMessage);
                window.open(`https://t.me/st1xloxServices_bot?text=${encodedMessage}`, '_blank');
                showNotification('Открывается Telegram для отправки сообщения', 'info');
            });
        };

        // Система отзывов с анимированными звездами
        const setupReviews = () => {
            // Функция для настройки звездного рейтинга
            const setupStarRating = (containerId, hiddenInputId) => {
                const stars = document.querySelectorAll(`#${containerId} .star`);
                const ratingInput = document.getElementById(hiddenInputId);
                
                stars.forEach(star => {
                    // При наведении
                    star.addEventListener('mouseover', function() {
                        const rating = parseInt(this.getAttribute('data-rating'));
                        
                        stars.forEach((s, index) => {
                            if (index < rating) {
                                s.classList.add('hover');
                            } else {
                                s.classList.remove('hover');
                            }
                        });
                    });
                    
                    // При уходе курсора
                    star.addEventListener('mouseout', function() {
                        stars.forEach(s => s.classList.remove('hover'));
                    });
                    
                    // При клике
                    star.addEventListener('click', function() {
                        const rating = parseInt(this.getAttribute('data-rating'));
                        ratingInput.value = rating;
                        
                        stars.forEach((s, index) => {
                            if (index < rating) {
                                s.classList.add('active');
                            } else {
                                s.classList.remove('active');
                            }
                        });
                    });
                });
            };
            
            // Настройка звезд для формы отзыва о заказе
            setupStarRating('order-rating-stars', 'review-order-rating');
            
            // Форма отзыва о заказе
            document.getElementById('order-review-form').addEventListener('submit', (e) => {
                e.preventDefault();
                
                const orderId = document.getElementById('review-order-id').value;
                const text = document.getElementById('review-order-text').value;
                const rating = parseInt(document.getElementById('review-order-rating').value);
                
                if (rating === 0) {
                    showNotification('Пожалуйста, поставьте оценку', 'warning');
                    return;
                }
                
                const currentUser = JSON.parse(localStorage.getItem('currentUser'));
                const reviews = JSON.parse(localStorage.getItem('reviews')) || [];
                const orders = JSON.parse(localStorage.getItem('orders')) || [];
                
                const newReview = {
                    id: reviews.length + 1,
                    name: currentUser.name,
                    text,
                    rating,
                    date: 'Только что',
                    approved: false,
                    orderId: parseInt(orderId)
                };
                
                reviews.unshift(newReview);
                localStorage.setItem('reviews', JSON.stringify(reviews));
                
                // Обновляем заказ, отмечаем что отзыв оставлен
                const orderIndex = orders.findIndex(o => o.id === parseInt(orderId));
                if (orderIndex !== -1) {
                    orders[orderIndex].hasReview = true;
                    localStorage.setItem('orders', JSON.stringify(orders));
                }
                
                // Закрываем модальное окно
                const modal = bootstrap.Modal.getInstance(document.getElementById('orderReviewModal'));
                modal.hide();
                
                showNotification('Отзыв о заказе успешно добавлен!', 'success');
                loadReviews();
                
                // Обновляем историю заказов
                if (currentUser) {
                    loadOrderHistory(currentUser.id);
                }
            });
        };

        // Система уведомлений
        const showNotification = (message, type = 'info') => {
            const notificationSystem = document.getElementById('notification-system');
            const notificationId = 'notification-' + Date.now();
            
            const notification = document.createElement('div');
            notification.className = `notification-item ${type}`;
            notification.id = notificationId;
            notification.innerHTML = `
                <div class="d-flex justify-content-between align-items-center">
                    <span>${message}</span>
                    <button class="btn-close btn-close-white" onclick="document.getElementById('${notificationId}').remove()"></button>
                </div>
            `;
            
            notificationSystem.appendChild(notification);
            
            setTimeout(() => {
                notification.classList.add('show');
            }, 10);
            
            setTimeout(() => {
                if (document.getElementById(notificationId)) {
                    notification.classList.remove('show');
                    setTimeout(() => {
                        if (document.getElementById(notificationId)) {
                            document.getElementById(notificationId).remove();
                        }
                    }, 300);
                }
            }, 5000);
        };

        // Улучшенные функции для админ-панели
        window.editUser = (userId) => {
            const users = JSON.parse(localStorage.getItem('users'));
            const user = users.find(u => u.id === userId);
            
            // Создаем модальное окно для редактирования пользователя
            const modalHtml = `
                <div class="modal fade" id="editUserModal" tabindex="-1" aria-hidden="true">
                    <div class="modal-dialog modal-dialog-centered">
                        <div class="modal-content glass-card">
                            <div class="modal-header">
                                <h5 class="modal-title">Редактирование пользователя: ${user.name}</h5>
                                <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                            </div>
                            <div class="modal-body">
                                <form id="edit-user-form">
                                    <div class="mb-3">
                                        <label for="edit-user-name" class="form-label">Имя</label>
                                        <input type="text" class="form-control" id="edit-user-name" value="${user.name}" required>
                                    </div>
                                    <div class="mb-3">
                                        <label for="edit-user-email" class="form-label">Email</label>
                                        <input type="email" class="form-control" id="edit-user-email" value="${user.email}" required>
                                    </div>
                                    <div class="mb-3">
                                        <label for="edit-user-role" class="form-label">Роль</label>
                                        <select class="form-select" id="edit-user-role">
                                            <option value="user" ${user.role === 'user' ? 'selected' : ''}>Пользователь</option>
                                            <option value="admin" ${user.role === 'admin' ? 'selected' : ''}>Администратор</option>
                                        </select>
                                    </div>
                                    <div class="mb-3">
                                        <label for="edit-user-status" class="form-label">Статус</label>
                                        <select class="form-select" id="edit-user-status">
                                            <option value="active" ${user.status === 'active' ? 'selected' : ''}>Активный</option>
                                            <option value="inactive" ${user.status === 'inactive' ? 'selected' : ''}>Неактивный</option>
                                        </select>
                                    </div>
                                    <button type="submit" class="btn btn-primary w-100">Сохранить изменения</button>
                                </form>
                            </div>
                        </div>
                    </div>
                </div>
            `;
            
            // Добавляем модальное окно в DOM
            document.body.insertAdjacentHTML('beforeend', modalHtml);
            
            // Показываем модальное окно
            const modal = new bootstrap.Modal(document.getElementById('editUserModal'));
            modal.show();
            
            // Обработчик формы редактирования
            document.getElementById('edit-user-form').addEventListener('submit', (e) => {
                e.preventDefault();
                
                const users = JSON.parse(localStorage.getItem('users'));
                const userIndex = users.findIndex(u => u.id === userId);
                
                if (userIndex !== -1) {
                    users[userIndex].name = document.getElementById('edit-user-name').value;
                    users[userIndex].email = document.getElementById('edit-user-email').value;
                    users[userIndex].role = document.getElementById('edit-user-role').value;
                    users[userIndex].status = document.getElementById('edit-user-status').value;
                    
                    localStorage.setItem('users', JSON.stringify(users));
                    updateAdminPanel();
                    modal.hide();
                    showNotification('Пользователь успешно обновлен', 'success');
                    
                    // Удаляем модальное окно из DOM
                    document.getElementById('editUserModal').remove();
                }
            });
            
            // Удаляем модальное окно при закрытии
            document.getElementById('editUserModal').addEventListener('hidden.bs.modal', () => {
                document.getElementById('editUserModal').remove();
            });
        };
        
        window.toggleUserStatus = (userId) => {
            const users = JSON.parse(localStorage.getItem('users'));
            const userIndex = users.findIndex(u => u.id === userId);
            
            if (userIndex !== -1) {
                users[userIndex].status = users[userIndex].status === 'active' ? 'inactive' : 'active';
                localStorage.setItem('users', JSON.stringify(users));
                updateAdminPanel();
                showNotification(`Статус пользователя изменен`, 'success');
            }
        };
        
        window.viewOrder = (orderId) => {
            const orders = JSON.parse(localStorage.getItem('orders'));
            const order = orders.find(o => o.id === orderId);
            
            if (!order) {
                showNotification('Заказ не найден', 'error');
                return;
            }
            
            const users = JSON.parse(localStorage.getItem('users'));
            const user = users.find(u => u.id === order.userId);
            
            // Создаем модальное окно для просмотра заказа
            const modalHtml = `
                <div class="modal fade" id="viewOrderModal" tabindex="-1" aria-hidden="true">
                    <div class="modal-dialog modal-dialog-centered modal-lg">
                        <div class="modal-content glass-card">
                            <div class="modal-header">
                                <h5 class="modal-title">Просмотр заказа #${order.id}</h5>
                                <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                            </div>
                            <div class="modal-body">
                                <div class="row">
                                    <div class="col-md-6">
                                        <p><strong>Пользователь:</strong> ${user ? user.name : 'Неизвестно'}</p>
                                        <p><strong>Email:</strong> ${user ? user.email : 'Неизвестно'}</p>
                                        <p><strong>Тип заказа:</strong> ${getOrderTypeName(order.type)}</p>
                                        <p><strong>Дата:</strong> ${order.date}</p>
                                    </div>
                                    <div class="col-md-6">
                                        <p><strong>Стоимость:</strong> ${order.price || 0} руб.</p>
                                        <p><strong>Статус:</strong> <span class="badge ${order.status === 'completed' ? 'bg-success' : order.status === 'pending' ? 'bg-warning' : 'bg-secondary'}">${order.status === 'completed' ? 'Выполнен' : order.status === 'pending' ? 'В обработке' : 'Отменен'}</span></p>
                                        <p><strong>Отзыв оставлен:</strong> ${order.hasReview ? 'Да' : 'Нет'}</p>
                                    </div>
                                </div>
                                <div class="mt-3">
                                    <h6>Детали заказа:</h6>
                                    <div class="p-3 bg-dark rounded">
                                        ${getOrderDetailsText(order)}
                                    </div>
                                </div>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Закрыть</button>
                                <button type="button" class="btn btn-primary" onclick="completeOrder(${order.id})">Завершить заказ</button>
                            </div>
                        </div>
                    </div>
                </div>
            `;
            
            // Добавляем модальное окно в DOM
            document.body.insertAdjacentHTML('beforeend', modalHtml);
            
            // Показываем модальное окно
            const modal = new bootstrap.Modal(document.getElementById('viewOrderModal'));
            modal.show();
            
            // Удаляем модальное окно при закрытии
            document.getElementById('viewOrderModal').addEventListener('hidden.bs.modal', () => {
                document.getElementById('viewOrderModal').remove();
            });
        };
        
        // Функция для получения текстового описания деталей заказа
        const getOrderDetailsText = (order) => {
            let details = '';
            
            switch(order.type) {
                case 'video':
                    details = `
                        <p><strong>Тип видео:</strong> ${order.serviceType === 'promo' ? 'Промо-ролик' : order.serviceType === 'intro' ? 'Интро/Аутро' : 'Футажи'}</p>
                        <p><strong>Продолжительность:</strong> ${order.data.videoDuration || 'Не указано'} секунд</p>
                        <p><strong>Стиль:</strong> ${order.data.style || 'Не указан'}</p>
                        <p><strong>Название проекта:</strong> ${order.data.title || 'Не указано'}</p>
                    `;
                    break;
                case 'images':
                    details = `
                        <p><strong>Тип изображения:</strong> ${order.serviceType === 'banner' ? 'Баннер' : order.serviceType === 'post' ? 'Пост для соц. сетей' : 'Пикчи'}</p>
                        <p><strong>Количество изображений:</strong> ${order.data.imageCount || 'Не указано'}</p>
                        <p><strong>Стиль:</strong> ${order.data.style || 'Не указан'}</p>
                        <p><strong>Название проекта:</strong> ${order.data.title || 'Не указано'}</p>
                    `;
                    break;
                case 'avatar':
                    details = `
                        <p><strong>Стиль аватарки:</strong> ${order.data.avatarStyle === 'anime' ? 'Аниме' : order.data.avatarStyle === 'movie' ? 'Фильм' : 'Сложная работа'}</p>
                        <p><strong>Описание/референс:</strong> ${order.data.avatarReference || 'Не указано'}</p>
                        <p><strong>Стиль:</strong> ${order.data.style || 'Не указан'}</p>
                        <p><strong>Название проекта:</strong> ${order.data.title || 'Не указано'}</p>
                    `;
                    break;
                case 'ads':
                    details = `
                        <p><strong>Продолжительность рекламы:</strong> ${order.data.adDuration || 'Не указано'} дней</p>
                        <p><strong>Текст рекламы:</strong> ${order.data.adText || 'Не указано'}</p>
                        <p><strong>Стиль:</strong> ${order.data.style || 'Не указан'}</p>
                        <p><strong>Название проекта:</strong> ${order.data.title || 'Не указано'}</p>
                    `;
                    break;
                default:
                    details = '<p>Информация о заказе недоступна</p>';
            }
            
            return details;
        };
        
        window.completeOrder = (orderId) => {
            const orders = JSON.parse(localStorage.getItem('orders'));
            const orderIndex = orders.findIndex(o => o.id === orderId);
            
            if (orderIndex !== -1) {
                orders[orderIndex].status = 'completed';
                localStorage.setItem('orders', JSON.stringify(orders));
                updateAdminPanel();
                showNotification(`Заказ #${orderId} завершен`, 'success');
                
                // Закрываем модальное окно просмотра заказа, если оно открыто
                const viewModal = document.getElementById('viewOrderModal');
                if (viewModal) {
                    const modal = bootstrap.Modal.getInstance(viewModal);
                    modal.hide();
                }
            }
        };

        window.approveReview = (reviewId) => {
            const reviews = JSON.parse(localStorage.getItem('reviews'));
            const reviewIndex = reviews.findIndex(r => r.id === reviewId);
            
            if (reviewIndex !== -1) {
                reviews[reviewIndex].approved = !reviews[reviewIndex].approved;
                localStorage.setItem('reviews', JSON.stringify(reviews));
                updateAdminPanel();
                loadReviews();
                showNotification(`Статус отзыва изменен`, 'success');
            }
        };

        window.deleteReview = (reviewId) => {
            const reviews = JSON.parse(localStorage.getItem('reviews'));
            const reviewIndex = reviews.findIndex(r => r.id === reviewId);
            
            if (reviewIndex !== -1) {
                reviews.splice(reviewIndex, 1);
                localStorage.setItem('reviews', JSON.stringify(reviews));
                updateAdminPanel();
                loadReviews();
                showNotification(`Отзыв удален`, 'success');
            }
        };

        // НОВАЯ ФУНКЦИЯ: Настройка кнопок админ-панели
        const setupAdminButtons = () => {
            // Кнопки виджетов админ-панели
            const adminButtons = [
                'admin-view-users-btn',
                'admin-add-user-btn',
                'admin-all-orders-btn',
                'admin-new-orders-btn',
                'admin-revenue-report-btn',
                'admin-export-revenue-btn',
                'admin-all-reviews-btn',
                'admin-moderate-reviews-btn'
            ];
            
            adminButtons.forEach(btnId => {
                const button = document.getElementById(btnId);
                if (button) {
                    button.addEventListener('click', function() {
                        // Показываем уведомление о функционале
                        const buttonText = this.textContent.trim();
                        showNotification(`Функция "${buttonText}" в разработке`, 'info');
                        
                        // Дополнительные действия для некоторых кнопок
                        if (btnId === 'admin-view-users-btn') {
                            document.getElementById('users-table').scrollIntoView({ behavior: 'smooth' });
                        } else if (btnId === 'admin-all-orders-btn') {
                            document.getElementById('orders-table').scrollIntoView({ behavior: 'smooth' });
                        } else if (btnId === 'admin-all-reviews-btn') {
                            document.getElementById('reviews-table').scrollIntoView({ behavior: 'smooth' });
                        }
                    });
                }
            });
            
            // Быстрые действия в админ-панели
            document.getElementById('quick-users').addEventListener('click', function() {
                document.getElementById('users-table').scrollIntoView({ behavior: 'smooth' });
                showNotification('Переход к управлению пользователями', 'info');
            });
            
            document.getElementById('quick-orders').addEventListener('click', function() {
                document.getElementById('orders-table').scrollIntoView({ behavior: 'smooth' });
                showNotification('Переход к управлению заказами', 'info');
            });
            
            document.getElementById('quick-revenue').addEventListener('click', function() {
                showNotification('Открытие аналитики доходов', 'info');
            });
            
            document.getElementById('quick-reviews').addEventListener('click', function() {
                document.getElementById('reviews-table').scrollIntoView({ behavior: 'smooth' });
                showNotification('Переход к модерации отзывов', 'info');
            });
            
            // Кнопка добавления пользователя
            document.getElementById('admin-add-user-btn2').addEventListener('click', function() {
                // Создаем модальное окно для добавления пользователя
                const modalHtml = `
                    <div class="modal fade" id="addUserModal" tabindex="-1" aria-hidden="true">
                        <div class="modal-dialog modal-dialog-centered">
                            <div class="modal-content glass-card">
                                <div class="modal-header">
                                    <h5 class="modal-title">Добавить пользователя</h5>
                                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal" aria-label="Close"></button>
                                </div>
                                <div class="modal-body">
                                    <form id="add-user-form">
                                        <div class="mb-3">
                                            <label for="add-user-name" class="form-label">Имя</label>
                                            <input type="text" class="form-control" id="add-user-name" required>
                                        </div>
                                        <div class="mb-3">
                                            <label for="add-user-email" class="form-label">Email</label>
                                            <input type="email" class="form-control" id="add-user-email" required>
                                        </div>
                                        <div class="mb-3">
                                            <label for="add-user-password" class="form-label">Пароль</label>
                                            <input type="password" class="form-control" id="add-user-password" required>
                                        </div>
                                        <div class="mb-3">
                                            <label for="add-user-role" class="form-label">Роль</label>
                                            <select class="form-select" id="add-user-role">
                                                <option value="user">Пользователь</option>
                                                <option value="admin">Администратор</option>
                                            </select>
                                        </div>
                                        <button type="submit" class="btn btn-primary w-100">Добавить пользователя</button>
                                    </form>
                                </div>
                            </div>
                        </div>
                    </div>
                `;
                
                // Добавляем модальное окно в DOM
                document.body.insertAdjacentHTML('beforeend', modalHtml);
                
                // Показываем модальное окно
                const modal = new bootstrap.Modal(document.getElementById('addUserModal'));
                modal.show();
                
                // Обработчик формы добавления пользователя
                document.getElementById('add-user-form').addEventListener('submit', (e) => {
                    e.preventDefault();
                    
                    const name = document.getElementById('add-user-name').value;
                    const email = document.getElementById('add-user-email').value;
                    const password = document.getElementById('add-user-password').value;
                    const role = document.getElementById('add-user-role').value;
                    
                    const users = JSON.parse(localStorage.getItem('users'));
                    const existingUser = users.find(u => u.email === email);
                    
                    if (existingUser) {
                        showNotification('Пользователь с таким email уже существует', 'error');
                        return;
                    }
                    
                    const newUser = {
                        id: users.length + 1,
                        name,
                        email,
                        password,
                        role,
                        status: 'active',
                        registrationDate: new Date().toISOString(),
                        bio: '',
                        onlineStatus: 'online',
                        avatar: null,
                        emailVerified: true
                    };
                    
                    users.push(newUser);
                    localStorage.setItem('users', JSON.stringify(users));
                    updateAdminPanel();
                    modal.hide();
                    showNotification('Пользователь успешно добавлен', 'success');
                    
                    // Удаляем модальное окно из DOM
                    document.getElementById('addUserModal').remove();
                });
                
                // Удаляем модальное окно при закрытии
                document.getElementById('addUserModal').addEventListener('hidden.bs.modal', () => {
                    document.getElementById('addUserModal').remove();
                });
            });
        };

        // Инициализация при загрузке страницы
        document.addEventListener('DOMContentLoaded', () => {
            initLocalStorage();
            setupNavigation();
            setupAuth();
            setupOrders();
            setupReviews();
            setupChat();
            setupAdminButtons();
            setupServiceRedirects();
            
            // Обработчик кнопки "Начать сейчас"
            document.getElementById('start-now-btn').addEventListener('click', function() {
                const currentUser = JSON.parse(localStorage.getItem('currentUser'));
                if (currentUser) {
                    showPage('dashboard');
                } else {
                    showPage('register');
                }
            });
            
            // Фильтрация заказов в админ-панели
            document.querySelectorAll('[data-order-filter]').forEach(btn => {
                btn.addEventListener('click', function() {
                    const filter = this.getAttribute('data-order-filter');
                    document.querySelectorAll('[data-order-filter]').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    // Здесь можно добавить логику фильтрации
                    showNotification(`Фильтр: ${filter === 'all' ? 'Все заказы' : filter === 'pending' ? 'В обработке' : 'Завершенные'}`, 'info');
                });
            });
            
            // Поиск пользователей в админ-панели
            document.getElementById('user-search').addEventListener('input', function() {
                const searchTerm = this.value.toLowerCase();
                const rows = document.querySelectorAll('#users-table tr');
                
                rows.forEach(row => {
                    const userName = row.cells[1].textContent.toLowerCase();
                    const userEmail = row.cells[2].textContent.toLowerCase();
                    
                    if (userName.includes(searchTerm) || userEmail.includes(searchTerm)) {
                        row.style.display = '';
                    } else {
                        row.style.display = 'none';
                    }
                });
            });
            
            // Фильтрация заказов в личном кабинете
            document.getElementById('orders-filter').addEventListener('change', function() {
                const filter = this.value;
                const orderCards = document.querySelectorAll('#orders-list .order-card');
                
                orderCards.forEach(card => {
                    const status = card.querySelector('.order-status').textContent.toLowerCase();
                    
                    if (filter === 'all' || 
                        (filter === 'completed' && status === 'выполнен') ||
                        (filter === 'pending' && status === 'в обработке')) {
                        card.style.display = 'block';
                    } else {
                        card.style.display = 'none';
                    }
                });
            });
            
            showPage('home');
            
            console.log('Данные для входа администратора:');
            console.log('Email: admin@st1xlox.com');
            console.log('Пароль: admin123');
            console.log('Email: moderator@st1xlox.com');
            console.log('Пароль: moderator123');
        });
    </script>
</body>
</html>
