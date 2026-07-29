[KELOMPOK 6 MATERI 2.html](https://github.com/user-attachments/files/30490416/KELOMPOK.6.MATERI.2.html)
<!DOCTYPE html>
<html lang="id" data-theme="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Media Pembelajaran Interaktif PAI & Budi Pekerti Kelas XII</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* ==========================================
           1. CSS VARIABLES & THEMING (PINK THEME)
           ========================================== */
        :root {
            /* Palette Warna Pink Modern */
            --primary-color: #ec4899;
            --primary-hover: #db2777;
            --primary-light: #fbcfe8;
            --primary-dark: #be185d;
            --secondary-color: #f43f5e;
            --accent-color: #fb7185;
            
            /* Status Colors */
            --success-color: #10b981;
            --warning-color: #f59e0b;
            --danger-color: #ef4444;
            --info-color: #3b82f6;

            /* Light Mode Variables */
            --bg-gradient: linear-gradient(135deg, #fdf2f8 0%, #fce7f3 50%, #fbcfe8 100%);
            --bg-surface: rgba(255, 255, 255, 0.85);
            --bg-card: rgba(255, 255, 255, 0.7);
            --text-main: #1f2937;
            --text-muted: #6b7280;
            --border-color: rgba(236, 72, 153, 0.2);
            --shadow-sm: 0 4px 6px -1px rgba(236, 72, 153, 0.05);
            --shadow-md: 0 10px 15px -3px rgba(236, 72, 153, 0.1);
            --shadow-lg: 0 20px 25px -5px rgba(236, 72, 153, 0.15);
            --glass-border: 1px solid rgba(255, 255, 255, 0.6);
            --sidebar-bg: rgba(255, 255, 255, 0.9);
            --header-bg: rgba(255, 255, 255, 0.8);
        }

        [data-theme="dark"] {
            /* Dark Mode Variables */
            --bg-gradient: linear-gradient(135deg, #18181b 0%, #27272a 50%, #3f3f46 100%);
            --bg-surface: rgba(24, 24, 27, 0.85);
            --bg-card: rgba(39, 39, 42, 0.7);
            --text-main: #f4f4f5;
            --text-muted: #a1a1aa;
            --border-color: rgba(244, 63, 94, 0.3);
            --shadow-sm: 0 4px 6px -1px rgba(0, 0, 0, 0.3);
            --shadow-md: 0 10px 15px -3px rgba(0, 0, 0, 0.4);
            --shadow-lg: 0 20px 25px -5px rgba(0, 0, 0, 0.5);
            --glass-border: 1px solid rgba(255, 255, 255, 0.1);
            --sidebar-bg: rgba(24, 24, 27, 0.95);
            --header-bg: rgba(24, 24, 27, 0.85);
        }

        /* RESET & BASE STYLES */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
            transition: background-color 0.3s ease, color 0.3s ease, border-color 0.3s ease;
        }

        body {
            background: var(--bg-gradient);
            background-attachment: fixed;
            color: var(--text-main);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            overflow-x: hidden;
        }

        /* GLASSMORPHISM CLASS */
        .glass {
            background: var(--bg-card);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: var(--glass-border);
            border-radius: 16px;
            box-shadow: var(--shadow-md);
        }

        /* ==========================================
           2. LOGIN PAGE STYLES
           ========================================== */
        #login-screen {
            position: fixed;
            inset: 0;
            z-index: 9999;
            background: var(--bg-gradient);
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .login-card {
            width: 100%;
            max-width: 440px;
            padding: 40px 30px;
            text-align: center;
            animation: floatIn 0.6s ease-out;
        }

        .login-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 36px;
            margin: 0 auto 20px;
            box-shadow: 0 10px 20px rgba(236, 72, 153, 0.3);
        }

        .login-title {
            font-size: 22px;
            font-weight: 700;
            color: var(--primary-dark);
            margin-bottom: 5px;
        }

        [data-theme="dark"] .login-title {
            color: var(--primary-light);
        }

        .login-subtitle {
            font-size: 13px;
            color: var(--text-muted);
            margin-bottom: 25px;
        }

        .form-group {
            margin-bottom: 18px;
            text-align: left;
        }

        .form-group label {
            display: block;
            font-size: 12px;
            font-weight: 600;
            margin-bottom: 6px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .input-wrapper {
            position: relative;
        }

        .input-wrapper i {
            position: absolute;
            left: 14px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--primary-color);
        }

        .form-control {
            width: 100%;
            padding: 12px 14px 12px 42px;
            border-radius: 10px;
            border: 1px solid var(--border-color);
            background: rgba(255, 255, 255, 0.6);
            color: var(--text-main);
            font-size: 14px;
            outline: none;
        }

        [data-theme="dark"] .form-control {
            background: rgba(0, 0, 0, 0.2);
        }

        .form-control:focus {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(236, 72, 153, 0.2);
        }

        .btn-primary {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 10px;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            font-size: 15px;
            font-weight: 600;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(236, 72, 153, 0.3);
            transition: all 0.3s ease;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 16px rgba(236, 72, 153, 0.4);
        }

        /* ==========================================
           3. MAIN LAYOUT (HEADER, SIDEBAR, CONTENT)
           ========================================== */
        #app-container {
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        /* Header Styles */
        .app-header {
            position: sticky;
            top: 0;
            z-index: 1000;
            height: 70px;
            padding: 0 24px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: var(--header-bg);
            backdrop-filter: blur(10px);
            border-bottom: var(--glass-border);
        }

        .header-left {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .btn-toggle-sidebar {
            background: none;
            border: none;
            font-size: 20px;
            color: var(--primary-color);
            cursor: pointer;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .btn-toggle-sidebar:hover {
            background: rgba(236, 72, 153, 0.1);
        }

        .header-title-box h1 {
            font-size: 16px;
            font-weight: 700;
            color: var(--primary-dark);
        }

        [data-theme="dark"] .header-title-box h1 {
            color: var(--primary-light);
        }

        .header-title-box p {
            font-size: 11px;
            color: var(--text-muted);
        }

        .header-right {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .user-badge {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 6px 12px;
            border-radius: 30px;
            background: rgba(236, 72, 153, 0.1);
            border: 1px solid var(--border-color);
        }

        .user-avatar {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            background: var(--primary-color);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 14px;
            font-weight: 600;
        }

        .user-info {
            display: flex;
            flex-direction: column;
            text-align: left;
        }

        .user-name {
            font-size: 12px;
            font-weight: 600;
        }

        .user-school {
            font-size: 10px;
            color: var(--text-muted);
        }

        .theme-toggle-btn {
            background: none;
            border: none;
            color: var(--text-main);
            font-size: 18px;
            cursor: pointer;
            width: 38px;
            height: 38px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid var(--border-color);
        }

        .theme-toggle-btn:hover {
            background: rgba(236, 72, 153, 0.1);
            color: var(--primary-color);
        }

        /* Body Container & Sidebar */
        .app-body {
            display: flex;
            flex: 1;
            position: relative;
        }

        .app-sidebar {
            width: 260px;
            background: var(--sidebar-bg);
            backdrop-filter: blur(12px);
            border-right: var(--glass-border);
            padding: 20px 15px;
            display: flex;
            flex-direction: column;
            transition: all 0.3s ease;
            z-index: 900;
        }

        .app-sidebar.collapsed {
            margin-left: -260px;
        }

        .sidebar-menu {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 6px;
        }

        .menu-item {
            display: flex;
            align-items: center;
            gap: 14px;
            padding: 12px 16px;
            border-radius: 12px;
            color: var(--text-main);
            font-size: 13.5px;
            font-weight: 500;
            text-decoration: none;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .menu-item i {
            font-size: 16px;
            width: 20px;
            text-align: center;
            color: var(--text-muted);
        }

        .menu-item:hover {
            background: rgba(236, 72, 153, 0.1);
            color: var(--primary-color);
        }

        .menu-item:hover i {
            color: var(--primary-color);
        }

        .menu-item.active {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            box-shadow: 0 4px 10px rgba(236, 72, 153, 0.25);
        }

        .menu-item.active i {
            color: white;
        }

        /* Sidebar Progress Card */
        .sidebar-progress-card {
            margin-top: auto;
            padding: 15px;
            border-radius: 12px;
            background: rgba(236, 72, 153, 0.08);
            border: 1px solid var(--border-color);
            text-align: center;
        }

        .progress-title {
            font-size: 12px;
            font-weight: 600;
            margin-bottom: 8px;
            display: flex;
            justify-content: space-between;
        }

        .progress-bar-bg {
            height: 8px;
            background: rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            overflow: hidden;
        }

        .progress-bar-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
            width: 0%;
            transition: width 0.5s ease;
        }

        /* Main Content Container */
        .main-content {
            flex: 1;
            padding: 25px;
            max-width: 1200px;
            margin: 0 auto;
            width: 100%;
            overflow-y: auto;
        }

        /* Breadcrumb Bar */
        .breadcrumb-container {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 12px;
            color: var(--text-muted);
            margin-bottom: 20px;
        }

        .breadcrumb-container i {
            font-size: 10px;
        }

        .breadcrumb-active {
            color: var(--primary-color);
            font-weight: 600;
        }

        /* Section Screen Wrapper */
        .section-screen {
            display: none;
            animation: fadeIn 0.4s ease-in-out;
        }

        .section-screen.active {
            display: block;
        }

        /* Card Section Header */
        .section-header {
            margin-bottom: 20px;
        }

        .section-header h2 {
            font-size: 22px;
            font-weight: 700;
            color: var(--primary-dark);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        [data-theme="dark"] .section-header h2 {
            color: var(--primary-light);
        }

        .section-header p {
            font-size: 13px;
            color: var(--text-muted);
            margin-top: 4px;
        }

        /* Grid Layouts */
        .grid-2 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 20px;
        }

        /* Standard Card Style */
        .content-card {
            padding: 24px;
            margin-bottom: 20px;
            position: relative;
            overflow: hidden;
        }

        /* ==========================================
           4. GAME: TEBAK GAMBAR (5 LEVELS)
           ========================================== */
        .game-container {
            max-width: 650px;
            margin: 0 auto;
            text-align: center;
        }

        .game-level-badge {
            display: inline-block;
            padding: 6px 16px;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            border-radius: 20px;
            font-size: 13px;
            font-weight: 600;
            margin-bottom: 15px;
        }

        .game-image-wrapper {
            width: 100%;
            height: 260px;
            border-radius: 16px;
            background: rgba(255, 255, 255, 0.8);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            border: 2px dashed var(--primary-color);
            position: relative;
            overflow: hidden;
        }

        .game-clue-icon {
            font-size: 70px;
            color: var(--primary-color);
            margin-bottom: 10px;
        }

        .game-clue-text {
            font-size: 14px;
            font-weight: 600;
            color: var(--text-main);
            padding: 0 20px;
        }

        .game-inputs {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin-bottom: 20px;
        }

        .game-input-text {
            text-align: center;
            letter-spacing: 2px;
            font-size: 18px;
            font-weight: 700;
            text-transform: uppercase;
            padding: 12px;
            width: 100%;
            max-width: 320px;
            border-radius: 10px;
            border: 2px solid var(--border-color);
            outline: none;
        }

        /* ==========================================
           5. PRACTICE & EVALUATION (QUIZ SYSTEM)
           ========================================== */
        .quiz-card {
            max-width: 750px;
            margin: 0 auto;
            padding: 30px;
        }

        .quiz-header-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 12px;
            border-bottom: 1px solid var(--border-color);
        }

        .quiz-timer {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 14px;
            font-weight: 700;
            color: var(--danger-color);
            background: rgba(239, 68, 68, 0.1);
            padding: 6px 14px;
            border-radius: 20px;
        }

        .question-text {
            font-size: 16px;
            font-weight: 600;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .options-list {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin-bottom: 25px;
        }

        .option-btn {
            display: flex;
            align-items: center;
            padding: 14px 18px;
            border-radius: 12px;
            background: rgba(255, 255, 255, 0.5);
            border: 1px solid var(--border-color);
            cursor: pointer;
            text-align: left;
            font-size: 14px;
            transition: all 0.2s ease;
        }

        [data-theme="dark"] .option-btn {
            background: rgba(0, 0, 0, 0.2);
        }

        .option-btn:hover {
            border-color: var(--primary-color);
            background: rgba(236, 72, 153, 0.08);
        }

        .option-btn.selected {
            border-color: var(--primary-color);
            background: rgba(236, 72, 153, 0.15);
            font-weight: 600;
        }

        .option-btn.correct {
            background: rgba(16, 185, 129, 0.2) !important;
            border-color: var(--success-color) !important;
            color: var(--success-color);
        }

        .option-btn.wrong {
            background: rgba(239, 68, 68, 0.2) !important;
            border-color: var(--danger-color) !important;
            color: var(--danger-color);
        }

        .option-prefix {
            width: 28px;
            height: 28px;
            border-radius: 50%;
            background: rgba(236, 72, 153, 0.15);
            color: var(--primary-color);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 12px;
            margin-right: 14px;
            flex-shrink: 0;
        }

        /* ==========================================
           6. FOOTER, TOAST, MODAL & SCROLL TOP
           ========================================== */
        .app-footer {
            text-align: center;
            padding: 20px;
            font-size: 12px;
            color: var(--text-muted);
            border-top: var(--glass-border);
            background: var(--header-bg);
            margin-top: auto;
        }

        /* Toast Notifications */
        #toast-container {
            position: fixed;
            bottom: 25px;
            right: 25px;
            z-index: 10000;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .toast {
            padding: 12px 20px;
            border-radius: 10px;
            background: white;
            color: #333;
            font-size: 13px;
            font-weight: 500;
            box-shadow: 0 5px 15px rgba(0,0,0,0.15);
            display: flex;
            align-items: center;
            gap: 10px;
            animation: slideIn 0.3s ease-out;
        }

        .toast-success { border-left: 5px solid var(--success-color); }
        .toast-error { border-left: 5px solid var(--danger-color); }
        .toast-info { border-left: 5px solid var(--info-color); }

        /* Scroll To Top Button */
        #btn-scroll-top {
            position: fixed;
            bottom: 25px;
            left: 25px;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: var(--primary-color);
            color: white;
            border: none;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            box-shadow: 0 4px 12px rgba(236, 72, 153, 0.4);
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            z-index: 999;
        }

        #btn-scroll-top.visible {
            opacity: 1;
            visibility: visible;
        }

        /* Confetti Canvas */
        #confetti-canvas {
            position: fixed;
            inset: 0;
            pointer-events: none;
            z-index: 99999;
        }

        /* Modal Styles */
        .modal-overlay {
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.5);
            backdrop-filter: blur(5px);
            z-index: 10000;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            opacity: 0;
            pointer-events: none;
            transition: all 0.3s ease;
        }

        .modal-overlay.active {
            opacity: 1;
            pointer-events: auto;
        }

        .modal-box {
            width: 100%;
            max-width: 500px;
            padding: 30px;
            text-align: center;
            transform: translateY(20px);
            transition: all 0.3s ease;
        }

        .modal-overlay.active .modal-box {
            transform: translateY(0);
        }

        /* Keyframe Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes floatIn {
            from { opacity: 0; transform: scale(0.95); }
            to { opacity: 1; transform: scale(1); }
        }

        @keyframes slideIn {
            from { opacity: 0; transform: translateX(50px); }
            to { opacity: 1; transform: translateX(0); }
        }

        /* Interactive Tabs */
        .tab-buttons {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 10px;
            overflow-x: auto;
        }

        .tab-btn {
            padding: 8px 16px;
            border: none;
            background: none;
            border-radius: 8px;
            font-size: 13px;
            font-weight: 600;
            color: var(--text-muted);
            cursor: pointer;
            white-space: nowrap;
        }

        .tab-btn.active {
            background: var(--primary-color);
            color: white;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        /* Accordion Style */
        .accordion-item {
            border: 1px solid var(--border-color);
            border-radius: 12px;
            margin-bottom: 10px;
            overflow: hidden;
        }

        .accordion-header {
            padding: 14px 18px;
            background: rgba(236, 72, 153, 0.05);
            font-weight: 600;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .accordion-body {
            padding: 16px 18px;
            font-size: 13.5px;
            line-height: 1.6;
            display: none;
        }

        .accordion-item.active .accordion-body {
            display: block;
        }

        /* RESPONSIVE MEDIA QUERIES */
        @media (max-width: 768px) {
            .app-sidebar {
                position: absolute;
                top: 70px;
                bottom: 0;
                left: 0;
                box-shadow: 10px 0 20px rgba(0,0,0,0.1);
            }
            .app-sidebar.collapsed {
                margin-left: -260px;
            }
            .main-content {
                padding: 15px;
            }
            .user-school {
                display: none;
            }
        }
    </style>
</head>
<body>

    <!-- CANVASES & OVERLAYS -->
    <canvas id="confetti-canvas"></canvas>
    <div id="toast-container"></div>

    <!-- 1. LOGIN SCREEN -->
    <div id="login-screen">
        <div class="login-card glass">
            <div class="login-icon">
                <i class="fa-solid fa-kaaba"></i>
            </div>
            <h2 class="login-title">PAI & Budi Pekerti XII</h2>
            <p class="login-subtitle">Integrasi Iman, Islam, dan Ihsan dalam Praktik Nyata</p>
            
            <form id="login-form">
                <div class="form-group">
                    <label for="student-name">Nama Lengkap Siswa</label>
                    <div class="input-wrapper">
                        <i class="fa-solid fa-user"></i>
                        <input type="text" id="student-name" class="form-control" placeholder="Masukkan nama lengkap..." required>
                    </div>
                </div>

                <div class="form-group">
                    <label for="school-name">Sekolah Asal</label>
                    <div class="input-wrapper">
                        <i class="fa-solid fa-school"></i>
                        <input type="text" id="school-name" class="form-control" placeholder="Contoh: SMAN 1 Probolinggo" required>
                    </div>
                </div>

                <div class="form-group">
                    <label for="secret-pin">PIN Akses (Default: 123456)</label>
                    <div class="input-wrapper">
                        <i class="fa-solid fa-key"></i>
                        <input type="password" id="secret-pin" class="form-control" placeholder="Masukkan 6 digit PIN" required>
                    </div>
                </div>

                <button type="submit" class="btn-primary">
                    <i class="fa-solid fa-right-to-bracket"></i> Masuk Pembelajaran
                </button>
            </form>
        </div>
    </div>

    <!-- 2. MAIN APPLICATION CONTAINER -->
    <div id="app-container">
        <!-- APP HEADER -->
        <header class="app-header">
            <div class="header-left">
                <button class="btn-toggle-sidebar" id="toggle-sidebar-btn" title="Buka/Tutup Menu">
                    <i class="fa-solid fa-bars"></i>
                </button>
                <div class="header-title-box">
                    <h1>PAI XII - Iman, Islam & Ihsan</h1>
                    <p>Semester Genap • MGMP PAI KAB PROB</p>
                </div>
            </div>

            <div class="header-right">
                <button class="theme-toggle-btn" id="theme-toggle" title="Ganti Mode Gelap/Terang">
                    <i class="fa-solid fa-moon"></i>
                </button>

                <div class="user-badge">
                    <div class="user-avatar" id="avatar-initial">S</div>
                    <div class="user-info">
                        <span class="user-name" id="display-user-name">Siswa</span>
                        <span class="user-school" id="display-user-school">Sekolah</span>
                    </div>
                </div>
            </div>
        </header>

        <div class="app-body">
            <!-- SIDEBAR MENU -->
            <aside class="app-sidebar" id="sidebar">
                <ul class="sidebar-menu">
                    <li><a class="menu-item active" data-target="screen-beranda"><i class="fa-solid fa-house"></i> Beranda</a></li>
                    <li><a class="menu-item" data-target="screen-petunjuk"><i class="fa-solid fa-circle-info"></i> Petunjuk</a></li>
                    <li><a class="menu-item" data-target="screen-materi"><i class="fa-solid fa-book-open"></i> Materi Interaktif</a></li>
                    <li><a class="menu-item" data-target="screen-game"><i class="fa-solid fa-gamepad"></i> Game Tebak Gambar</a></li>
                    <li><a class="menu-item" data-target="screen-latihan"><i class="fa-solid fa-pen-to-square"></i> Latihan Soal</a></li>
                    <li><a class="menu-item" data-target="screen-evaluasi"><i class="fa-solid fa-file-signature"></i> Evaluasi Quiz</a></li>
                    <li><a class="menu-item" data-target="screen-ringkasan"><i class="fa-solid fa-list-check"></i> Ringkasan</a></li>
                    <li><a class="menu-item" data-target="screen-referensi"><i class="fa-solid fa-bookmark"></i> Referensi</a></li>
                    <li><a class="menu-item" data-target="screen-profil"><i class="fa-solid fa-users"></i> Profil Penyusun</a></li>
                </ul>

                <div class="sidebar-progress-card">
                    <div class="progress-title">
                        <span>Progress Belajar</span>
                        <span id="sidebar-progress-percent">0%</span>
                    </div>
                    <div class="progress-bar-bg">
                        <div class="progress-bar-fill" id="sidebar-progress-bar"></div>
                    </div>
                </div>
            </aside>

            <!-- MAIN CONTENT AREA -->
            <main class="main-content">
                <!-- BREADCRUMB -->
                <div class="breadcrumb-container">
                    <i class="fa-solid fa-house"></i>
                    <span>/</span>
                    <span id="breadcrumb-title" class="breadcrumb-active">Beranda</span>
                </div>

                <!-- SECTION 1: BERANDA -->
                <section id="screen-beranda" class="section-screen active">
                    <div class="section-header">
                        <h2><i class="fa-solid fa-heart-pulse"></i> Selamat Datang di Media Pembelajaran</h2>
                        <p>Mari memahami dan mengintegrasikan Iman, Islam, dan Ihsan dalam kehidupan nyata sehari-hari.</p>
                    </div>

                    <div class="content-card glass">
                        <h3 style="color: var(--primary-dark); margin-bottom: 10px;">Tujuan Pembelajaran</h3>
                        <ul style="padding-left: 20px; font-size: 14px; line-height: 1.8; color: var(--text-main);">
                            <li>Meyakini kebenaran hubungan Iman, Islam, dan Ihsan dalam praktik nyata kehidupan sehari-hari.</li>
                            <li>Merefleksikan keterkaitan dan integrasi Iman, Islam, dan Ihsan dalam kehidupan sehari-hari.</li>
                            <li>Mengamalkan karakter berakhlak mulia berbasis pilar-pilar ajaran Islam.</li>
                        </ul>
                    </div>

                    <div class="grid-3">
                        <div class="content-card glass" style="text-align: center;">
                            <i class="fa-solid fa-brain" style="font-size: 40px; color: var(--primary-color); margin-bottom: 10px;"></i>
                            <h4>Iman (Aqidah)</h4>
                            <p style="font-size: 12px; color: var(--text-muted); margin-top: 5px;">Keyakinan dan pembenaran dalam hati yang mendasari setiap niat & tindakan.</p>
                        </div>
                        <div class="content-card glass" style="text-align: center;">
                            <i class="fa-solid fa-hands-praying" style="font-size: 40px; color: var(--secondary-color); margin-bottom: 10px;"></i>
                            <h4>Islam (Syariah)</h4>
                            <p style="font-size: 12px; color: var(--text-muted); margin-top: 5px;">Praktik peribadatan dan hukum syariat yang nampak dalam perbuatan fisik.</p>
                        </div>
                        <div class="content-card glass" style="text-align: center;">
                            <i class="fa-solid fa-gem" style="font-size: 40px; color: var(--accent-color); margin-bottom: 10px;"></i>
                            <h4>Ihsan (Akhlak)</h4>
                            <p style="font-size: 12px; color: var(--text-muted); margin-top: 5px;">Kesempurnaan perbuatan dengan merasa senantiasa diawasi oleh Allah SWT.</p>
                        </div>
                    </div>
                </section>

                <!-- SECTION 2: PETUNJUK -->
                <section id="screen-petunjuk" class="section-screen">
                    <div class="section-header">
                        <h2><i class="fa-solid fa-circle-info"></i> Petunjuk Penggunaan</h2>
                        <p>Panduan langkah demi langkah untuk memaksimalkan pengalaman belajar Anda.</p>
                    </div>

                    <div class="content-card glass">
                        <div class="accordion-item active">
                            <div class="accordion-header">
                                <span><i class="fa-solid fa-1"></i> Navigasi Aplikasi</span>
                                <i class="fa-solid fa-chevron-down"></i>
                            </div>
                            <div class="accordion-body">
                                Gunakan menu sidebar di sebelah kiri (atau klik ikon hamburger di perangkat seluler) untuk berpindah antar modul pembelajaran.
                            </div>
                        </div>

                        <div class="accordion-item">
                            <div class="accordion-header">
                                <span><i class="fa-solid fa-2"></i> Penguasaan Materi</span>
                                <i class="fa-solid fa-chevron-down"></i>
                            </div>
                            <div class="accordion-body">
                                Bacalah materi interaktif yang disajikan dalam bentuk tab. Setiap tab menjelaskan pondasi, hubungan, serta integrasi Iman, Islam, dan Ihsan.
                            </div>
                        </div>

                        <div class="accordion-item">
                            <div class="accordion-header">
                                <span><i class="fa-solid fa-3"></i> Game & Latihan</span>
                                <i class="fa-solid fa-chevron-down"></i>
                            </div>
                            <div class="accordion-body">
                                Selesaikan Game Tebak Gambar (5 level) dan Latihan Soal (10 butir) untuk menguji pemahaman dasar Anda sebelum melangkah ke Evaluasi.
                            </div>
                        </div>

                        <div class="accordion-item">
                            <div class="accordion-header">
                                <span><i class="fa-solid fa-4"></i> Ujian Evaluasi & Sertifikat</span>
                                <i class="fa-solid fa-chevron-down"></i>
                            </div>
                            <div class="accordion-body">
                                Kerjakan Evaluasi Soal (10 butir) dalam batas waktu 15 menit. Setelah selesai, skor Anda akan dihitung secara otomatis dan progres disimpan.
                            </div>
                        </div>
                    </div>
                </section>

                <!-- SECTION 3: MATERI INTERAKTIF -->
                <section id="screen-materi" class="section-screen">
                    <div class="section-header">
                        <h2><i class="fa-solid fa-book-open"></i> Materi Interaktif</h2>
                        <p>Integrasi Tiga Pilar Agama: Iman, Islam, dan Ihsan dalam Praktik Nyata.</p>
                    </div>

                    <div class="content-card glass">
                        <div class="tab-buttons">
                            <button class="tab-btn active" onclick="switchTab('tab-hakikat')">1. Hakikat & Definisi</button>
                            <button class="tab-btn" onclick="switchTab('tab-keterkaitan')">2. Keterkaitan & Trilogis</button>
                            <button class="tab-btn" onclick="switchTab('tab-praktik')">3. Praktik Nyata Sehari-hari</button>
                        </div>

                        <!-- Tab 1 -->
                        <div id="tab-hakikat" class="tab-content active">
                            <h3 style="color: var(--primary-dark); margin-bottom: 12px;">Hakikat Iman, Islam, dan Ihsan (Hadits Jibril)</h3>
                            <p style="font-size: 14px; line-height: 1.7; margin-bottom: 15px;">
                                Berdasarkan <strong>Hadits Riwayat Muslim (Hadits ke-2 Arba'in An-Nawawi)</strong>, malaikat Jibril datang mengajarkan agama kepada para sahabat melalui tiga pertanyaan kunci kepada Rasulullah SAW:
                            </p>
                            
                            <div class="grid-3" style="margin-top: 15px;">
                                <div style="background: rgba(236,72,153,0.1); padding: 15px; border-radius: 12px; border-left: 4px solid var(--primary-color);">
                                    <h4 style="color: var(--primary-dark);">1. Iman (Keyakinan)</h4>
                                    <p style="font-size: 12.5px; margin-top: 8px;">Membenarkan dengan hati, diikrarkan dengan lisan, dan diamalkan dengan anggota badan. Mencakup 6 Rukun Iman.</p>
                                </div>
                                <div style="background: rgba(244,63,94,0.1); padding: 15px; border-radius: 12px; border-left: 4px solid var(--secondary-color);">
                                    <h4 style="color: var(--secondary-color);">2. Islam (Pengabdian)</h4>
                                    <p style="font-size: 12.5px; margin-top: 8px;">Tunduk dan taat pada hukum Allah SWT melalui perbuatan lahiriah. Mencakup 5 Rukun Islam.</p>
                                </div>
                                <div style="background: rgba(251,113,133,0.1); padding: 15px; border-radius: 12px; border-left: 4px solid var(--accent-color);">
                                    <h4 style="color: var(--primary-dark);">3. Ihsan (Kesempurnaan)</h4>
                                    <p style="font-size: 12.5px; margin-top: 8px;">"Engkau menyembah Allah seolah-olah melihat-Nya; jika tidak bisa, ketahuilah Dia melihatmu."</p>
                                </div>
                            </div>
                        </div>

                        <!-- Tab 2 -->
                        <div id="tab-keterkaitan" class="tab-content">
                            <h3 style="color: var(--primary-dark); margin-bottom: 12px;">Analogi Segitiga Tritunggal Ajaran Islam</h3>
                            <p style="font-size: 14px; line-height: 1.7; margin-bottom: 15px;">
                                Ketiga unsur ini tidak dapat dipisahkan. Jika dianalogikan dengan sebuah pohon yang rindang:
                            </p>
                            <div style="padding: 20px; background: rgba(255,255,255,0.4); border-radius: 12px; line-height: 1.8; font-size: 14px;">
                                <p><strong> Akar Pohon = IMAN:</strong> Fondasi tersembunyi di dalam tanah (hati). Tanpa akar yang kuat, pohon akan roboh.</p>
                                <p><strong> Batang & Dahan = ISLAM:</strong> Wujud fisik yang nampak di atas tanah (ibadah ritual dan syariat).</p>
                                <p><strong> Buah yang Manis = IHSAN:</strong> Hasil keindahan akhlak dan kualitas ibadah yang dirasakan manfaatnya oleh lingkungan sekitar.</p>
                            </div>
                        </div>

                        <!-- Tab 3 -->
                        <div id="tab-praktik" class="tab-content">
                            <h3 style="color: var(--primary-dark); margin-bottom: 12px;">Penerapan Ihsan dalam Kehidupan Modern</h3>
                            <ul style="line-height: 1.8; font-size: 14px; padding-left: 20px;">
                                <li><strong>Ihsan kepada Allah:</strong> Sholat dengan khusyuk dan tidak terburu-buru karena merasa Allah memperhatikan.</li>
                                <li><strong>Ihsan kepada Sesama Manusia:</strong> Berkata sopan, jujur saat ujian, dan suka menolong tanpa pamrih.</li>
                                <li><strong>Ihsan kepada Alam Lingkungan:</strong> Tidak membuang sampah sembarangan dan menjaga kelestarian alam sebagai amanah khalifah.</li>
                            </ul>
                        </div>
                    </div>
                </section>

                <!-- SECTION 4: GAME TEBAK GAMBAR -->
                <section id="screen-game" class="section-screen">
                    <div class="section-header">
                        <h2><i class="fa-solid fa-gamepad"></i> Game Tebak Gambar</h2>
                        <p>Tebak istilah atau penerapan dari gambar clue di bawah ini! (5 Level)</p>
                    </div>

                    <div class="content-card glass game-container">
                        <div class="game-level-badge" id="game-level-display">LEVEL 1 dari 5</div>
                        
                        <div class="game-image-wrapper">
                            <i class="fa-solid fa-hand-holding-heart game-clue-icon" id="game-clue-icon"></i>
                            <div class="game-clue-text" id="game-clue-text">Perbuatan memberi bantuan kepada sesama dengan ikhlas sebagai wujud Ihsan.</div>
                        </div>

                        <div class="game-inputs">
                            <input type="text" id="game-answer-input" class="game-input-text" placeholder="KETIK JAWABAN..." autocomplete="off">
                        </div>

                        <button class="btn-primary" onclick="checkGameAnswer()" style="max-width: 200px; margin: 0 auto;">
                            <i class="fa-solid fa-check"></i> Periksa Jawaban
                        </button>
                    </div>
                </section>

                <!-- SECTION 5: LATIHAN SOAL -->
                <section id="screen-latihan" class="section-screen">
                    <div class="section-header">
                        <h2><i class="fa-solid fa-pen-to-square"></i> Latihan Soal Interaktif</h2>
                        <p>Uji pemahaman Anda dengan 10 soal latihan beserta umpan balik langsung.</p>
                    </div>

                    <div class="content-card glass quiz-card">
                        <div class="quiz-header-bar">
                            <span style="font-weight: 600;" id="latihan-counter">Soal 1 dari 10</span>
                            <span style="font-weight: 600; color: var(--primary-color);" id="latihan-score">Skor: 0</span>
                        </div>

                        <div class="question-text" id="latihan-question-text">
                            Loading pertanyaan latihan...
                        </div>

                        <div class="options-list" id="latihan-options-container">
                            <!-- Populated dynamically -->
                        </div>

                        <div id="latihan-feedback" style="display: none; padding: 12px; border-radius: 10px; margin-bottom: 15px; font-size: 13.5px;"></div>

                        <button class="btn-primary" id="btn-next-latihan" onclick="nextLatihanQuestion()" style="display: none;">
                            Pertanyaan Selanjutnya <i class="fa-solid fa-arrow-right"></i>
                        </button>
                    </div>
                </section>

                <!-- SECTION 6: EVALUASI QUIZ -->
                <section id="screen-evaluasi" class="section-screen">
                    <div class="section-header">
                        <h2><i class="fa-solid fa-file-signature"></i> Ujian Evaluasi</h2>
                        <p>Kerjakan 10 soal evaluasi dengan timer otomatis 15 menit.</p>
                    </div>

                    <div id="evaluasi-start-card" class="content-card glass" style="text-align: center; max-width: 600px; margin: 0 auto;">
                        <i class="fa-solid fa-stopwatch" style="font-size: 60px; color: var(--primary-color); margin-bottom: 15px;"></i>
                        <h3>Siap Memulai Ujian Evaluasi?</h3>
                        <p style="font-size: 13.5px; color: var(--text-muted); margin: 10px 0 20px;">
                            Ujian terdiri dari 10 soal pilihan ganda dengan durasi waktu 15 menit. Hasil akan disimpan ke rekap belajar Anda.
                        </p>
                        <button class="btn-primary" onclick="startEvaluasiQuiz()" style="max-width: 220px; margin: 0 auto;">
                            <i class="fa-solid fa-play"></i> Mulai Evaluasi
                        </button>
                    </div>

                    <div id="evaluasi-quiz-card" class="content-card glass quiz-card" style="display: none;">
                        <div class="quiz-header-bar">
                            <span style="font-weight: 600;" id="evaluasi-counter">Soal 1 dari 10</span>
                            <div class="quiz-timer">
                                <i class="fa-solid fa-clock"></i>
                                <span id="evaluasi-timer">15:00</span>
                            </div>
                        </div>

                        <div class="question-text" id="evaluasi-question-text">
                            Loading pertanyaan evaluasi...
                        </div>

                        <div class="options-list" id="evaluasi-options-container">
                            <!-- Populated dynamically -->
                        </div>

                        <button class="btn-primary" id="btn-next-evaluasi" onclick="nextEvaluasiQuestion()" style="margin-top: 10px;">
                            Simpan & Lanjut <i class="fa-solid fa-arrow-right"></i>
                        </button>
                    </div>
                </section>

                <!-- SECTION 7: RINGKASAN -->
                <section id="screen-ringkasan" class="section-screen">
                    <div class="section-header">
                        <h2><i class="fa-solid fa-list-check"></i> Ringkasan Pembelajaran</h2>
                        <p>Rangkuman pokok materi integrasi Iman, Islam, dan Ihsan.</p>
                    </div>

                    <div class="content-card glass">
                        <ul style="line-height: 2; font-size: 14px; padding-left: 20px;">
                            <li><strong>Iman</strong> adalah pondasi keyakinan batiniah yang mengarahkan niat manusia.</li>
                            <li><strong>Islam</strong> adalah ekspresi fisik dari keimanan yang diwujudkan melalui pelaksanaan ibadah ritual & syariat.</li>
                            <li><strong>Ihsan</strong> adalah tingkatan kualitas spiritual tertinggi di mana seseorang senantiasa beribadah dan berbuat baik karena merasa dihadiri/diawasi oleh Allah SWT.</li>
                            <li>Ketiganya membentuk kesatuan utuh: Tanpa Iman, ibadah Islam tidak bernilai; tanpa Islam, Iman tidak berbukti; tanpa Ihsan, ibadah kehilangan keikhlasan.</li>
                        </ul>
                    </div>
                </section>

                <!-- SECTION 8: REFERENSI -->
                <section id="screen-referensi" class="section-screen">
                    <div class="section-header">
                        <h2><i class="fa-solid fa-bookmark"></i> Referensi Valid & Legal</h2>
                        <p>Sumber rujukan materi pembelajaran PAI Kelas XII.</p>
                    </div>

                    <div class="content-card glass">
                        <ol style="line-height: 2; font-size: 13.5px; padding-left: 20px;">
                            <li>Al-Qur'an al-Karim dan Terjemahannya, Kementerian Agama Republik Indonesia.</li>
                            <li>Buku Teks Utama PAI dan Budi Pekerti SMA/SMK Kelas XII, Kemendikbudristek RI, Kurikulum Merdeka.</li>
                            <li>Kitab Al-Arba'in An-Nawawiyah, Imam An-Nawawi (Hadits ke-2 tentang Iman, Islam, dan Ihsan).</li>
                            <li>Syarah Arba'in An-Nawawi, Syaikh Muhammad bin Shalih al-Utsaimin.</li>
                        </ol>
                    </div>
                </section>

                <!-- SECTION 9: PROFIL PENYUSUN -->
                <section id="screen-profil" class="section-screen">
                    <div class="section-header">
                        <h2><i class="fa-solid fa-users"></i> Profil Tim Penyusun</h2>
                        <p>Pengembang Media Pembelajaran Interaktif PAI & Budi Pekerti.</p>
                    </div>

                    <div class="content-card glass" style="text-align: center;">
                        <div style="width: 90px; height: 90px; background: linear-gradient(135deg, var(--primary-color), var(--secondary-color)); color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 38px; margin: 0 auto 15px;">
                            <i class="fa-solid fa-user-group"></i>
                        </div>
                        <h3 style="color: var(--primary-dark); font-size: 20px;">KELOMPOK 6</h3>
                        <p style="font-size: 14px; font-weight: 600; color: var(--text-muted); margin-top: 4px;">MGMP PAI KAB PROBOLINGGO</p>
                        
                        <div style="margin-top: 20px; padding-top: 20px; border-top: 1px solid var(--border-color); font-size: 13.5px; line-height: 1.8;">
                            <p><strong>Mata Pelajaran:</strong> PAI dan Budi Pekerti</p>
                            <p><strong>Sasaran:</strong> Kelas XII SMA / SMK (Semester Genap)</p>
                            <p><strong>Wilayah Kerja:</strong> Musyawarah Guru Mata Pelajaran (MGMP) PAI Kab. Probolinggo</p>
                        </div>
                    </div>
                </section>
            </main>
        </div>

        <!-- APP FOOTER -->
        <footer class="app-footer">
            &copy; 2026 Media Pembelajaran Interaktif PAI Kelas XII • Kelompok 6 MGMP PAI KAB PROB
        </footer>
    </div>

    <!-- SCROLL TO TOP BUTTON -->
    <button id="btn-scroll-top" title="Kembali ke atas">
        <i class="fa-solid fa-arrow-up"></i>
    </button>

    <!-- MODAL POPUP REKAP HASIL -->
    <div class="modal-overlay" id="result-modal">
        <div class="modal-box glass">
            <i class="fa-solid fa-trophy" style="font-size: 60px; color: var(--warning-color); margin-bottom: 15px;"></i>
            <h2 id="modal-result-title">Hasil Evaluasi</h2>
            <p id="modal-result-subtitle" style="font-size: 13px; color: var(--text-muted); margin: 6px 0 20px;"></p>
            
            <div style="font-size: 36px; font-weight: 800; color: var(--primary-color); margin-bottom: 15px;" id="modal-result-score">
                0
            </div>

            <p id="modal-result-message" style="font-size: 13.5px; line-height: 1.6; margin-bottom: 20px;"></p>

            <button class="btn-primary" onclick="closeResultModal()">
                Tutup & Lihat Rekap
            </button>
        </div>
    </div>

    <!-- ==========================================
       JAVASCRIPT LOGIC & APPLICATION STATE
       ========================================== -->
    <script>
        /* CONFIGURATION & CONSTANTS */
        const SECRET_PIN = "123456"; // Easy to change PIN

        /* DATA: GAME TEBAK GAMBAR (5 LEVELS) */
        const gameData = [
            {
                level: 1,
                icon: "fa-hand-holding-heart",
                clue: "Perbuatan memberi bantuan kepada sesama dengan ikhlas sebagai wujud nyata Ihsan.",
                answers: ["SEDEKAH", "INFAQ", "IHSAN"]
            },
            {
                level: 2,
                icon: "fa-person-praying",
                clue: "Rukun Islam kedua yang dilaksanakan secara berjamaah untuk memakmurkan masjid.",
                answers: ["SHALAT", "SALAT", "SHOLAT"]
            },
            {
                level: 3,
                icon: "fa-book-quran",
                clue: "Kitab suci petunjuk umat Islam yang wajib diimani dan diamalkan isi kandungannya.",
                answers: ["ALQURAN", "AL-QURAN", "AL QURAN", "KITAB"]
            },
            {
                level: 4,
                icon: "fa-seedling",
                clue: "Bentuk Ihsan kepada lingkungan dengan merawat tanaman dan menjaga kebersihan alam.",
                answers: ["KEBERSIHAN", "PELESTARIAN", "IHSAN ALAM", "LINGKUNGAN"]
            },
            {
                level: 5,
                icon: "fa-people-roof",
                clue: "Sikap berbakti kepada kedua orang tua sebagai perintah keimanan dan akhlak mulia.",
                answers: ["BIRRUL WALIDAYN", "BERBAKTI", "TAAT ORANG TUA"]
            }
        ];

        /* DATA: LATIHAN SOAL (10 ITEMS) */
        const latihanQuestions = [
            {
                q: "Menurut Hadits Riwayat Muslim dari Umar bin Khattab RA, siapakah sosok yang datang bertanya tentang Iman, Islam, dan Ihsan kepada Nabi?",
                options: ["Malaikat Mikail", "Malaikat Jibril", "Malaikat Israfil", "Sahabat Abu Bakar"],
                answer: 1,
                exp: "Malaikat Jibril datang menyamar menyerupai laki-laki berpakaian sangat putih untuk mengajarkan agama."
            },
            {
                q: "Ibadah ritual fisik seperti mengucapkan dua kalimat syahadat dan mendirikan shalat termasuk ke dalam pilar...",
                options: ["Iman", "Islam", "Ihsan", "Taqwa"],
                answer: 1,
                exp: "Islam merupakan penyerahan diri secara lahiriah melalui perbuatan fisik dan ibadah syariat."
            },
            {
                q: "Definisi Ihsan yang dijelaskan oleh Rasulullah SAW dalam Hadits Jibril adalah...",
                options: [
                    "Meyakini dalam hati tanpa keraguan sedikitpun",
                    "Beribadah seolah melihat Allah atau merasa diawasi oleh-Nya",
                    "Menghafal 99 Asmaul Husna",
                    "Membayar zakat dan menunaikan ibadah haji"
                ],
                answer: 1,
                exp: "Ihsan adalah menyembah Allah seakan-akan melihat-Nya, dan jika tidak bisa, meyakini bahwa Allah melihat kita."
            },
            {
                q: "Sikap jujur ketika mengerjakan ujian tanpa pengawasan guru merupakan contoh penerapan Ihsan karena merasa...",
                options: ["Diawasi oleh kamera CCTV", "Takut dimusuhi teman", "Muroqobah (Merasa diawasi oleh Allah SWT)", "Ingin mendapatkan pujian"],
                answer: 2,
                exp: "Merasa senantiasa diawasi Allah SWT (Muroqobah) adalah inti dari sikap Ihsan."
            },
            {
                q: "Di bawah ini yang merupakan contoh bentuk Ihsan kepada lingkungan alam adalah...",
                options: [
                    "Menebang pohon secara liar untuk ekonomi",
                    "Menjaga kebersihan dan menanam kebaikan lingkungan",
                    "Membuang sampah ke sungai kecil",
                    "Membakar sampah plastik di pemukiman"
                ],
                answer: 1,
                exp: "Menjaga kelestarian dan kebersihan alam adalah amanah khalifah sebagai wujud Ihsan."
            },
            {
                q: "Keterkaitan antara Iman, Islam, dan Ihsan sering dianalogikan sebagai sebuah pohon. Manakah yang menjadi AKAR pohon?",
                options: ["Ihsan", "Islam", "Iman", "Akhlak"],
                answer: 2,
                exp: "Iman adalah fondasi batiniah yang mengokohkan seluruh amalan (seperti akar pohon)."
            },
            {
                q: "Seorang muslim beribadah rajin tetapi suka berbuat zalim dan mencela sesama. Hal ini menunjukkan kurangnya kesempurnaan pada pilar...",
                options: ["Islam", "Ihsan", "Syariat", "Sertifikasi"],
                answer: 1,
                exp: "Ihsan memancarkan keindahan akhlak mulia dalam hubungan antarsesama makhluk."
            },
            {
                q: "Rukun Iman terdiri dari berapa perkara?",
                options: ["5 Perkara", "6 Perkara", "7 Perkara", "12 Perkara"],
                answer: 1,
                exp: "Rukun Iman berjumlah 6 perkara (Iman kepada Allah, Malaikat, Kitab, Rasul, Hari Akhir, Qada & Qadar)."
            },
            {
                q: "Berikut adalah wujud nyata Ihsan kepada sesama manusia, KECUALI...",
                options: ["Membantu tetangga yang tertimpa musibah", "Menyebarkan kabar bohong (hoaks)", "Berbicara dengan kata-kata yang santun", "Menghormati orang yang lebih tua"],
                answer: 1,
                exp: "Menyebarkan hoaks adalah tindakan tercela yang bertentangan dengan prinsip Ihsan."
            },
            {
                q: "Mengapa tiga pilar (Iman, Islam, Ihsan) harus diintegrasikan dalam kehidupan?",
                options: [
                    "Agar diakui sebagai ustaz kondang",
                    "Agar membentuk pribadi muslim yang kaffah (utuh)",
                    "Agar terbebas dari pajak negara",
                    "Hanya sebagai syarat kelulusan mata pelajaran PAI"
                ],
                answer: 1,
                exp: "Ketiga pilar tersebut merupakan satu kesatuan utuh untuk menjadi muslim kaffah."
            }
        ];

        /* DATA: EVALUASI SOAL (10 ITEMS) */
        const evaluasiQuestions = [
            {
                q: "Hubungan antara Iman dan Islam dipahami sebagai dua hal yang...",
                options: ["Saling bertentangan", "Tidak berhubungan", "Saling melengkapi dan terikat erat", "Hanya berlaku pada zaman nabi"],
                answer: 2
            },
            {
                q: "Seseorang yang mengaku beriman namun enggan menjalankan ibadah shalat dan zakat mengalami ketimpangan pada dimensi...",
                options: ["Ihsan", "Islam (Syariat)", "Budaya", "Ekonomi"],
                answer: 1
            },
            {
                q: "Prinsip Muroqobah dalam Ihsan berdampak langsung pada terbentuknya karakter...",
                options: ["Integritas dan kejujuran", "Sombong dan konsumtif", "Pedes dan acuh tak acuh", "Pesimis dalam hidup"],
                answer: 0
            },
            {
                q: "Perbuatannya nampak beribadah khusyuk di depan orang banyak, namun berbuat maksiat saat sendiri. Perbuatan ini dinamakan...",
                options: ["Ihsan", "Riya' / Nifak", "Tawakal", "Qana'ah"],
                answer: 1
            },
            {
                q: "Menyembelih hewan ternak dengan pisau yang tajam agar tidak menyiksa hewan merupakan bentuk Ihsan kepada...",
                options: ["Manusia", "Binatang / Hewan", "Tumbuhan", "Malaikat"],
                answer: 1
            },
            {
                q: "Manakah tingkatan Ihsan yang paling tinggi menurut penjelasan para ulama?",
                options: ["Makam Muroqobah (Merasa diawasi)", "Makam Musyahadah (Seolah melihat Allah)", "Makam Taqlid", "Makam Sabar"],
                answer: 1
            },
            {
                q: "Inti dari Rukun Islam yang pertama adalah pengakuan kesaksian...",
                options: ["Tauhid dan Kerasulan Nabi Muhammad SAW", "Kewajiban Puasa", "Kewajiban Zakat", "Perjalanan Isra Mi'raj"],
                answer: 0
            },
            {
                q: "Buah manis dari penerapan Ihsan dalam kehidupan bermasyarakat adalah terwujudnya...",
                options: ["Perselisihan antar warga", "Keharmonisan dan kedamaian", "Kesenjangan sosial", "Keangkuhan kelompok"],
                answer: 1
            },
            {
                q: "Mengimani takdir baik dan takdir buruk Allah SWT merupakan bagian dari pilar...",
                options: ["Islam", "Iman", "Ihsan", "Syariat"],
                answer: 1
            },
            {
                q: "Integrasi Iman, Islam, dan Ihsan dalam era digital dapat diwujudkan melalui...",
                options: ["Mengunggah ujaran kebencian di sosmed", "Menggunakan media sosial untuk menyebar kebaikan dan kebenaran", "Menghabiskan waktu dengan game tanpa shalat", "Membocorkan data pribadi orang lain"],
                answer: 1
            }
        ];

        /* APPLICATION STATE */
        let state = {
            studentName: '',
            schoolName: '',
            currentGameLevel: 0,
            latihanIndex: 0,
            latihanScore: 0,
            evaluasiIndex: 0,
            evaluasiScore: 0,
            evaluasiAnswers: [],
            evaluasiTimerSeconds: 900, // 15 mins
            timerInterval: null
        };

        /* WEB AUDIO SYNTHESIZER (NO EXTERNAL AUDIO FILES NEEDED) */
        const audioCtx = new (window.AudioContext || window.webkitAudioContext)();

        function playSound(type) {
            if (audioCtx.state === 'suspended') {
                audioCtx.resume();
            }
            const osc = audioCtx.createOscillator();
            const gain = audioCtx.createGain();
            osc.connect(gain);
            gain.connect(audioCtx.destination);

            const now = audioCtx.currentTime;

            if (type === 'click') {
                osc.type = 'sine';
                osc.frequency.setValueAtTime(400, now);
                gain.gain.setValueAtTime(0.1, now);
                gain.gain.exponentialRampToValueAtTime(0.01, now + 0.05);
                osc.start(now);
                osc.stop(now + 0.05);
            } else if (type === 'correct') {
                osc.type = 'triangle';
                osc.frequency.setValueAtTime(523.25, now); // C5
                osc.frequency.setValueAtTime(659.25, now + 0.1); // E5
                osc.frequency.setValueAtTime(783.99, now + 0.2); // G5
                gain.gain.setValueAtTime(0.2, now);
                gain.gain.exponentialRampToValueAtTime(0.01, now + 0.4);
                osc.start(now);
                osc.stop(now + 0.4);
            } else if (type === 'wrong') {
                osc.type = 'sawtooth';
                osc.frequency.setValueAtTime(220, now); // A3
                osc.frequency.setValueAtTime(180, now + 0.15);
                gain.gain.setValueAtTime(0.2, now);
                gain.gain.exponentialRampToValueAtTime(0.01, now + 0.3);
                osc.start(now);
                osc.stop(now + 0.3);
            }
        }

        /* INITIALIZATION & LOCALSTORAGE */
        document.addEventListener("DOMContentLoaded", () => {
            loadSavedData();
            setupEventListeners();
            initTheme();
        });

        function loadSavedData() {
            const savedName = localStorage.getItem("pai_student_name");
            const savedSchool = localStorage.getItem("pai_school_name");

            if (savedName && savedSchool) {
                state.studentName = savedName;
                state.schoolName = savedSchool;
                document.getElementById("login-screen").style.display = "none";
                updateUserDisplay();
                updateProgress();
            }
        }

        function setupEventListeners() {
            // Login Form Submit
            document.getElementById("login-form").addEventListener("submit", (e) => {
                e.preventDefault();
                const name = document.getElementById("student-name").value.trim();
                const school = document.getElementById("school-name").value.trim();
                const pin = document.getElementById("secret-pin").value.trim();

                if (pin !== SECRET_PIN) {
                    showToast("PIN Salah! Gunakan PIN default: 123456", "error");
                    playSound('wrong');
                    return;
                }

                state.studentName = name;
                state.schoolName = school;
                localStorage.setItem("pai_student_name", name);
                localStorage.setItem("pai_school_name", school);

                document.getElementById("login-screen").style.display = "none";
                updateUserDisplay();
                showToast("Berhasil login! Selamat belajar.", "success");
                playSound('correct');
                updateProgress();
            });

            // Sidebar Navigation
            document.querySelectorAll(".menu-item").forEach(item => {
                item.addEventListener("click", (e) => {
                    playSound('click');
                    const target = item.getAttribute("data-target");
                    
                    document.querySelectorAll(".menu-item").forEach(m => m.classList.remove("active"));
                    item.classList.add("active");

                    document.querySelectorAll(".section-screen").forEach(s => s.classList.remove("active"));
                    const activeScreen = document.getElementById(target);
                    if (activeScreen) activeScreen.classList.add("active");

                    // Update Breadcrumb
                    const title = item.innerText.trim();
                    document.getElementById("breadcrumb-title").innerText = title;

                    // Trigger specific screen init
                    if (target === "screen-game") initGameLevel();
                    if (target === "screen-latihan") initLatihan();

                    // Close sidebar on mobile
                    if (window.innerWidth <= 768) {
                        document.getElementById("sidebar").classList.add("collapsed");
                    }
                });
            });

            // Toggle Sidebar Button
            document.getElementById("toggle-sidebar-btn").addEventListener("click", () => {
                playSound('click');
                document.getElementById("sidebar").classList.toggle("collapsed");
            });

            // Dark/Light Theme Toggle
            document.getElementById("theme-toggle").addEventListener("click", () => {
                playSound('click');
                const currentTheme = document.documentElement.getAttribute("data-theme");
                const newTheme = currentTheme === "dark" ? "light" : "dark";
                document.documentElement.setAttribute("data-theme", newTheme);
                localStorage.setItem("pai_theme", newTheme);
                updateThemeIcon(newTheme);
            });

            // Scroll To Top
            window.addEventListener("scroll", () => {
                const btn = document.getElementById("btn-scroll-top");
                if (window.scrollY > 300) btn.classList.add("visible");
                else btn.classList.remove("visible");
            });

            document.getElementById("btn-scroll-top").addEventListener("click", () => {
                playSound('click');
                window.scrollTo({ top: 0, behavior: "smooth" });
            });
        }

        function initTheme() {
            const savedTheme = localStorage.getItem("pai_theme") || "light";
            document.documentElement.setAttribute("data-theme", savedTheme);
            updateThemeIcon(savedTheme);
        }

        function updateThemeIcon(theme) {
            const icon = document.querySelector("#theme-toggle i");
            if (theme === "dark") {
                icon.className = "fa-solid fa-sun";
            } else {
                icon.className = "fa-solid fa-moon";
            }
        }

        function updateUserDisplay() {
            document.getElementById("display-user-name").innerText = state.studentName;
            document.getElementById("display-user-school").innerText = state.schoolName;
            document.getElementById("avatar-initial").innerText = state.studentName.charAt(0).toUpperCase();
        }

        function updateProgress() {
            let progress = 20; // Initial progress upon login
            if (state.currentGameLevel > 0) progress += (state.currentGameLevel / 5) * 25;
            if (state.latihanIndex > 0) progress += 25;
            if (state.evaluasiScore > 0) progress += 30;

            progress = Math.min(progress, 100);
            document.getElementById("sidebar-progress-percent").innerText = `${Math.round(progress)}%`;
            document.getElementById("sidebar-progress-bar").style.width = `${progress}%`;
        }

        /* TAB SWITCHER */
        function switchTab(tabId) {
            playSound('click');
            document.querySelectorAll(".tab-btn").forEach(btn => btn.classList.remove("active"));
            document.querySelectorAll(".tab-content").forEach(content => content.classList.remove("active"));

            event.target.classList.add("active");
            document.getElementById(tabId).classList.add("active");
        }

        /* TOAST NOTIFICATION SYSTEM */
        function showToast(message, type = "info") {
            const container = document.getElementById("toast-container");
            const toast = document.createElement("div");
            toast.className = `toast toast-${type}`;
            
            let iconClass = "fa-circle-info";
            if (type === "success") iconClass = "fa-circle-check";
            if (type === "error") iconClass = "fa-circle-xmark";

            toast.innerHTML = `<i class="fa-solid ${iconClass}"></i> <span>${message}</span>`;
            container.appendChild(toast);

            setTimeout(() => {
                toast.remove();
            }, 3000);
        }

        /* GAME: TEBAK GAMBAR LOGIC */
        function initGameLevel() {
            if (state.currentGameLevel >= gameData.length) {
                state.currentGameLevel = 0; // Loop or reset
            }
            const data = gameData[state.currentGameLevel];
            document.getElementById("game-level-display").innerText = `LEVEL ${data.level} dari 5`;
            document.getElementById("game-clue-icon").className = `fa-solid ${data.icon} game-clue-icon`;
            document.getElementById("game-clue-text").innerText = data.clue;
            document.getElementById("game-answer-input").value = "";
        }

        function checkGameAnswer() {
            const userInput = document.getElementById("game-answer-input").value.trim().toUpperCase();
            const currentLevelData = gameData[state.currentGameLevel];

            if (!userInput) {
                showToast("Ketik jawaban terlebih dahulu!", "error");
                return;
            }

            if (currentLevelData.answers.includes(userInput)) {
                playSound('correct');
                triggerConfetti();
                showToast("Jawaban Benar! Selamat!", "success");
                state.currentGameLevel++;
                updateProgress();

                if (state.currentGameLevel < gameData.length) {
                    setTimeout(() => {
                        initGameLevel();
                    }, 1200);
                } else {
                    showToast("Luar biasa! Kamu telah menyelesaikan semua level Game!", "success");
                }
            } else {
                playSound('wrong');
                showToast("Jawaban kurang tepat. Coba lagi!", "error");
            }
        }

        /* LATIHAN SOAL LOGIC */
        function initLatihan() {
            state.latihanIndex = 0;
            state.latihanScore = 0;
            renderLatihanQuestion();
        }

        function renderLatihanQuestion() {
            const q = latihanQuestions[state.latihanIndex];
            document.getElementById("latihan-counter").innerText = `Soal ${state.latihanIndex + 1} dari ${latihanQuestions.length}`;
            document.getElementById("latihan-score").innerText = `Skor: ${state.latihanScore}`;
            document.getElementById("latihan-question-text").innerText = q.q;

            const container = document.getElementById("latihan-options-container");
            container.innerHTML = "";

            document.getElementById("latihan-feedback").style.display = "none";
            document.getElementById("btn-next-latihan").style.display = "none";

            const prefixes = ["A", "B", "C", "D"];
            q.options.forEach((opt, idx) => {
                const btn = document.createElement("button");
                btn.className = "option-btn";
                btn.innerHTML = `<span class="option-prefix">${prefixes[idx]}</span> <span>${opt}</span>`;
                btn.onclick = () => selectLatihanOption(idx);
                container.appendChild(btn);
            });
        }

        function selectLatihanOption(selectedIdx) {
            const q = latihanQuestions[state.latihanIndex];
            const buttons = document.querySelectorAll("#latihan-options-container .option-btn");

            buttons.forEach(btn => btn.style.pointerEvents = "none");

            if (selectedIdx === q.answer) {
                playSound('correct');
                buttons[selectedIdx].classList.add("correct");
                state.latihanScore += 10;
                document.getElementById("latihan-score").innerText = `Skor: ${state.latihanScore}`;
                showLatihanFeedback(true, q.exp);
            } else {
                playSound('wrong');
                buttons[selectedIdx].classList.add("wrong");
                buttons[q.answer].classList.add("correct");
                showLatihanFeedback(false, q.exp);
            }

            document.getElementById("btn-next-latihan").style.display = "inline-flex";
            updateProgress();
        }

        function showLatihanFeedback(isCorrect, exp) {
            const box = document.getElementById("latihan-feedback");
            box.style.display = "block";
            if (isCorrect) {
                box.style.background = "rgba(16, 185, 129, 0.15)";
                box.style.color = "var(--success-color)";
                box.innerHTML = `<strong><i class="fa-solid fa-circle-check"></i> Jawaban Tepat!</strong> ${exp}`;
            } else {
                box.style.background = "rgba(239, 68, 68, 0.15)";
                box.style.color = "var(--danger-color)";
                box.innerHTML = `<strong><i class="fa-solid fa-circle-xmark"></i> Kurang Tepat.</strong> ${exp}`;
            }
        }

        function nextLatihanQuestion() {
            playSound('click');
            state.latihanIndex++;
            if (state.latihanIndex < latihanQuestions.length) {
                renderLatihanQuestion();
            } else {
                showToast(`Latihan Selesai! Total Skor Anda: ${state.latihanScore}`, "success");
                triggerConfetti();
            }
        }

        /* EVALUASI QUIZ & TIMER LOGIC */
        function startEvaluasiQuiz() {
            playSound('click');
            document.getElementById("evaluasi-start-card").style.display = "none";
            document.getElementById("evaluasi-quiz-card").style.display = "block";

            state.evaluasiIndex = 0;
            state.evaluasiScore = 0;
            state.evaluasiAnswers = [];
            state.evaluasiTimerSeconds = 900; // 15 mins

            startEvaluasiTimer();
            renderEvaluasiQuestion();
        }

        function startEvaluasiTimer() {
            clearInterval(state.timerInterval);
            state.timerInterval = setInterval(() => {
                state.evaluasiTimerSeconds--;
                const mins = Math.floor(state.evaluasiTimerSeconds / 60);
                const secs = state.evaluasiTimerSeconds % 60;
                document.getElementById("evaluasi-timer").innerText = `${mins.toString().padStart(2, '0')}:${secs.toString().padStart(2, '0')}`;

                if (state.evaluasiTimerSeconds <= 0) {
                    clearInterval(state.timerInterval);
                    finishEvaluasi();
                }
            }, 1000);
        }

        function renderEvaluasiQuestion() {
            const q = evaluasiQuestions[state.evaluasiIndex];
            document.getElementById("evaluasi-counter").innerText = `Soal ${state.evaluasiIndex + 1} dari ${evaluasiQuestions.length}`;
            document.getElementById("evaluasi-question-text").innerText = q.q;

            const container = document.getElementById("evaluasi-options-container");
            container.innerHTML = "";

            const prefixes = ["A", "B", "C", "D"];
            q.options.forEach((opt, idx) => {
                const btn = document.createElement("button");
                btn.className = "option-btn";
                btn.innerHTML = `<span class="option-prefix">${prefixes[idx]}</span> <span>${opt}</span>`;
                btn.onclick = () => {
                    playSound('click');
                    document.querySelectorAll("#evaluasi-options-container .option-btn").forEach(b => b.classList.remove("selected"));
                    btn.classList.add("selected");
                    state.evaluasiAnswers[state.evaluasiIndex] = idx;
                };
                container.appendChild(btn);
            });
        }

        function nextEvaluasiQuestion() {
            if (state.evaluasiAnswers[state.evaluasiIndex] === undefined) {
                showToast("Pilih salah satu jawaban terlebih dahulu!", "error");
                return;
            }

            state.evaluasiIndex++;
            if (state.evaluasiIndex < evaluasiQuestions.length) {
                renderEvaluasiQuestion();
            } else {
                finishEvaluasi();
            }
        }

        function finishEvaluasi() {
            clearInterval(state.timerInterval);
            
            // Calculate Score
            let correctCount = 0;
            evaluasiQuestions.forEach((q, idx) => {
                if (state.evaluasiAnswers[idx] === q.answer) {
                    correctCount++;
                }
            });

            state.evaluasiScore = correctCount * 10;
            updateProgress();

            // Show Modal Results
            document.getElementById("modal-result-score").innerText = state.evaluasiScore;
            document.getElementById("modal-result-subtitle").innerText = `Siswa: ${state.studentName} (${state.schoolName})`;
            
            const msg = document.getElementById("modal-result-message");
            if (state.evaluasiScore >= 75) {
                msg.innerText = "Selamat! Anda telah mencapai Kriteria Ketuntasan Minimal (KKM). Terus pertahankan semangat belajar dan amalkan nilai-nilai Ihsan!";
                triggerConfetti();
                playSound('correct');
            } else {
                msg.innerText = "Anda belum mencapai KKM. Silakan pelajari kembali materi interaktif dan coba lagi ujian evaluasi ini.";
                playSound('wrong');
            }

            document.getElementById("result-modal").classList.add("active");
        }

        function closeResultModal() {
            playSound('click');
            document.getElementById("result-modal").classList.remove("active");
            document.getElementById("evaluasi-quiz-card").style.display = "none";
            document.getElementById("evaluasi-start-card").style.display = "block";
        }

        /* ACCORDION TOGGLE FUNCTION */
        document.addEventListener("click", (e) => {
            const header = e.target.closest(".accordion-header");
            if (header) {
                playSound('click');
                const item = header.parentElement;
                item.classList.toggle("active");
            }
        });

        /* CANVAS CONFETTI EFFECT (VANILLA JS SYNTHESIZED) */
        function triggerConfetti() {
            const canvas = document.getElementById("confetti-canvas");
            const ctx = canvas.getContext("2d");
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;

            const particles = [];
            const colors = ["#ec4899", "#f43f5e", "#fb7185", "#3b82f6", "#10b981", "#f59e0b"];

            for (let i = 0; i < 80; i++) {
                particles.push({
                    x: canvas.width / 2,
                    y: canvas.height / 2,
                    vx: (Math.random() - 0.5) * 12,
                    vy: (Math.random() - 0.7) * 12,
                    size: Math.random() * 8 + 4,
                    color: colors[Math.floor(Math.random() * colors.length)],
                    life: 100
                });
            }

            function animate() {
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                let alive = false;

                particles.forEach(p => {
                    if (p.life > 0) {
                        alive = true;
                        p.x += p.vx;
                        p.y += p.vy;
                        p.vy += 0.2; // gravity
                        p.life--;

                        ctx.fillStyle = p.color;
                        ctx.beginPath();
                        ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
                        ctx.fill();
                    }
                });

                if (alive) {
                    requestAnimationFrame(animate);
                } else {
                    ctx.clearRect(0, 0, canvas.width, canvas.height);
                }
            }

            animate();
        }
    </script>
</body>
</html>
