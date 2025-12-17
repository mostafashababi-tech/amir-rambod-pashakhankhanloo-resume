# amir-rambod-pashakhankhanloo-resume
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>رزومه معماری امیررامبد پاشاخانلو</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;600;700;800&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Vazirmatn', sans-serif;
            background: #000;
            min-height: 100vh;
            padding: 40px 20px;
            overflow-x: hidden;
            position: relative;
        }
        
        /* انیمیشن معماری - ساختمان‌های متحرک */
        .architecture-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            overflow: hidden;
            opacity: 0.15;
        }
        
        .building {
            position: absolute;
            bottom: 0;
            background: linear-gradient(180deg, rgba(78, 205, 196, 0.3) 0%, rgba(69, 183, 209, 0.5) 100%);
            animation: buildingRise 3s ease-out forwards;
            border-top: 3px solid rgba(78, 205, 196, 0.6);
        }
        
        .building::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: repeating-linear-gradient(
                0deg,
                transparent,
                transparent 25px,
                rgba(255,255,255,0.1) 25px,
                rgba(255,255,255,0.1) 27px
            );
        }
        
        .building::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: repeating-linear-gradient(
                90deg,
                transparent,
                transparent 30px,
                rgba(255,255,255,0.05) 30px,
                rgba(255,255,255,0.05) 32px
            );
        }
        
        @keyframes buildingRise {
            from {
                transform: translateY(100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
        
        .building:nth-child(1) { left: 5%; width: 80px; height: 250px; animation-delay: 0s; }
        .building:nth-child(2) { left: 15%; width: 120px; height: 350px; animation-delay: 0.3s; }
        .building:nth-child(3) { left: 28%; width: 90px; height: 280px; animation-delay: 0.6s; }
        .building:nth-child(4) { left: 42%; width: 110px; height: 320px; animation-delay: 0.9s; }
        .building:nth-child(5) { left: 58%; width: 95px; height: 290px; animation-delay: 1.2s; }
        .building:nth-child(6) { left: 72%; width: 130px; height: 380px; animation-delay: 1.5s; }
        .building:nth-child(7) { left: 88%; width: 85px; height: 260px; animation-delay: 1.8s; }
        
        /* خطوط معماری پرسپکتیو */
        .perspective-lines {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            opacity: 0.08;
        }
        
        .line {
            position: absolute;
            height: 1px;
            background: linear-gradient(90deg, transparent, #4ecdc4, transparent);
            animation: lineMove 8s linear infinite;
            transform-origin: center;
        }
        
        @keyframes lineMove {
            0% { transform: translateY(-20px) scaleX(0.8); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: translateY(100vh) scaleX(1.5); opacity: 0; }
        }
        
        .line:nth-child(1) { top: 0%; left: 10%; width: 60%; animation-delay: 0s; }
        .line:nth-child(2) { top: 15%; left: 20%; width: 50%; animation-delay: 2s; }
        .line:nth-child(3) { top: 30%; left: 15%; width: 55%; animation-delay: 4s; }
        .line:nth-child(4) { top: 45%; left: 25%; width: 45%; animation-delay: 6s; }
        
        /* ذرات معلق */
        .floating-particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            pointer-events: none;
        }
        
        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: #4ecdc4;
            border-radius: 50%;
            opacity: 0.5;
            animation: float 15s infinite ease-in-out;
        }
        
        @keyframes float {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            25% { transform: translate(100px, -100px) rotate(90deg); }
            50% { transform: translate(50px, -200px) rotate(180deg); }
            75% { transform: translate(-50px, -150px) rotate(270deg); }
        }
        
        .particle:nth-child(1) { left: 10%; top: 20%; animation-delay: 0s; }
        .particle:nth-child(2) { left: 30%; top: 40%; animation-delay: 3s; }
        .particle:nth-child(3) { left: 50%; top: 60%; animation-delay: 6s; }
        .particle:nth-child(4) { left: 70%; top: 30%; animation-delay: 9s; }
        .particle:nth-child(5) { left: 90%; top: 50%; animation-delay: 12s; }
        
        .resume-container {
            max-width: 1400px;
            margin: 0 auto;
            background: linear-gradient(145deg, #ffffff 0%, #f5f7fa 100%);
            border-radius: 40px;
            overflow: hidden;
            box-shadow: 0 40px 120px rgba(78, 205, 196, 0.4), 0 0 80px rgba(69, 183, 209, 0.2);
            position: relative;
            z-index: 1;
        }
        
        .resume-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                linear-gradient(45deg, transparent 48%, rgba(78, 205, 196, 0.03) 50%, transparent 52%),
                linear-gradient(-45deg, transparent 48%, rgba(69, 183, 209, 0.03) 50%, transparent 52%);
            background-size: 20px 20px;
            pointer-events: none;
        }
        
        .header {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
            padding: 80px 60px;
            position: relative;
            overflow: hidden;
        }
        
        /* شبکه سه بعدی پس‌زمینه */
        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(78, 205, 196, 0.1) 2px, transparent 2px),
                linear-gradient(90deg, rgba(78, 205, 196, 0.1) 2px, transparent 2px);
            background-size: 50px 50px;
            transform: perspective(500px) rotateX(60deg);
            transform-origin: center bottom;
            animation: gridPulse 3s ease-in-out infinite;
        }
        
        @keyframes gridPulse {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 0.6; }
        }
        
        .header-content {
            display: flex;
            align-items: center;
            gap: 50px;
            position: relative;
            z-index: 2;
        }
        
        .photo-section {
            position: relative;
        }
        
        .photo-container {
            width: 220px;
            height: 220px;
            border-radius: 30px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 20px 60px rgba(78, 205, 196, 0.4);
            background: linear-gradient(135deg, #4ecdc4 0%, #45b7d1 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            border: 5px solid rgba(255,255,255,0.1);
            transition: all 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55);
        }
        
        .photo-container:hover {
            transform: scale(1.05) rotate(5deg);
            box-shadow: 0 30px 80px rgba(78, 205, 196, 0.6);
        }
        
        .photo-container::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.3), transparent);
            transform: rotate(45deg);
            animation: photoShine 3s linear infinite;
        }
        
        @keyframes photoShine {
            0% { transform: translateX(-100%) rotate(45deg); }
            100% { transform: translateX(100%) rotate(45deg); }
        }
        
        #profilePhoto {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: none;
        }
        
        #profilePhoto.loaded {
            display: block;
        }
        
        .photo-placeholder {
            color: white;
            font-size: 4em;
            opacity: 0.8;
        }
        
        .upload-btn {
            position: absolute;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            background: linear-gradient(135deg, #4ecdc4 0%, #45b7d1 100%);
            color: white;
            padding: 10px 20px;
            border-radius: 20px;
            cursor: pointer;
            font-size: 0.85em;
            font-weight: 600;
            box-shadow: 0 5px 20px rgba(78, 205, 196, 0.4);
            transition: all 0.3s;
            white-space: nowrap;
        }
        
        .upload-btn:hover {
            transform: translateX(-50%) translateY(-3px);
            box-shadow: 0 8px 30px rgba(78, 205, 196, 0.6);
        }
        
        #photoUpload {
            display: none;
        }
        
        .name-section {
            flex: 1;
        }
        
        .name {
            font-size: 4.5em;
            font-weight: 800;
            background: linear-gradient(120deg, #fff 0%, #4ecdc4 50%, #fff 100%);
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 15px;
            animation: nameGradient 4s ease infinite;
            text-shadow: 0 0 40px rgba(78, 205, 196, 0.5);
            letter-spacing: 2px;
        }
        
        @keyframes nameGradient {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        
        .title {
            font-size: 2em;
            color: #4ecdc4;
            font-weight: 400;
            letter-spacing: 4px;
            margin-bottom: 10px;
            animation: fadeInUp 1s ease-out 0.3s both;
        }
        
        .subtitle {
            color: #45b7d1;
            font-size: 1.1em;
            margin-bottom: 30px;
            font-weight: 300;
            animation: fadeInUp 1s ease-out 0.6s both;
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .contact-info {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            animation: fadeInUp 1s ease-out 0.9s both;
        }
        
        .contact-item {
            color: #ccc;
            display: flex;
            align-items: center;
            gap: 12px;
            transition: all 0.3s;
            padding: 12px 20px;
            border-radius: 25px;
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(78, 205, 196, 0.2);
            font-size: 0.95em;
        }
        
        .contact-item:hover {
            color: #4ecdc4;
            background: rgba(78, 205, 196, 0.15);
            transform: translateX(-5px);
            border-color: #4ecdc4;
            box-shadow: 0 5px 20px rgba(78, 205, 196, 0.3);
        }
        
        .main-content {
            display: grid;
            grid-template-columns: 1.2fr 1fr;
            gap: 60px;
            padding: 60px;
        }
        
        .section {
            margin-bottom: 45px;
            animation: slideInRight 0.8s ease-out;
        }
        
        @keyframes slideInRight {
            from {
                opacity: 0;
                transform: translateX(30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        .section-title {
            font-size: 2em;
            font-weight: 700;
            margin-bottom: 30px;
            position: relative;
            padding-bottom: 20px;
            color: #1a1a2e;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            right: 0;
            width: 100px;
            height: 5px;
            background: linear-gradient(90deg, #4ecdc4, #45b7d1);
            border-radius: 3px;
            animation: lineGrow 1s ease-out;
        }
        
        @keyframes lineGrow {
            from { width: 0; }
            to { width: 100px; }
        }
        
        .section-icon {
            font-size: 1.3em;
        }
        
        .about-text {
            color: #444;
            line-height: 2;
            font-size: 1.05em;
            padding: 30px;
            background: linear-gradient(135deg, #f8f9fa 0%, #fff 100%);
            border-radius: 25px;
            border-right: 5px solid #4ecdc4;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            position: relative;
            overflow: hidden;
        }
        
        .about-text::before {
            content: '"';
            position: absolute;
            top: 10px;
            right: 20px;
            font-size: 5em;
            color: rgba(78, 205, 196, 0.1);
            font-family: Georgia, serif;
        }
        
        .experience-item {
            margin-bottom: 30px;
            padding: 30px;
            background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
            border-radius: 25px;
            border-right: 6px solid transparent;
            border-image: linear-gradient(135deg, #4ecdc4, #45b7d1) 1;
            box-shadow: 0 8px 25px rgba(0,0,0,0.06);
            transition: all 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            position: relative;
            overflow: hidden;
        }
        
        .experience-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(78, 205, 196, 0.1), transparent);
            transition: left 0.5s;
        }
        
        .experience-item:hover::before {
            left: 100%;
        }
        
        .experience-item:hover {
            transform: translateX(-8px) translateY(-5px);
            box-shadow: 0 15px 40px rgba(78, 205, 196, 0.25);
        }
        
        .job-title {
            font-size: 1.4em;
            font-weight: 700;
            color: #1a1a2e;
            margin-bottom: 10px;
        }
        
        .company {
            color: #4ecdc4;
            font-weight: 600;
            margin-bottom: 10px;
            font-size: 1.1em;
        }
        
        .duration {
            color: #636e72;
            font-size: 0.95em;
            margin-bottom: 15px;
            font-style: italic;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .description {
            color: #555;
            line-height: 1.9;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
        }
        
        .skill-item {
            background: linear-gradient(135deg, #4ecdc4 0%, #45b7d1 100%);
            color: white;
            padding: 20px 25px;
            border-radius: 20px;
            text-align: center;
            font-weight: 700;
            font-size: 1.05em;
            box-shadow: 0 8px 20px rgba(78, 205, 196, 0.4);
            transition: all 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            position: relative;
            overflow: hidden;
        }
        
        .skill-item::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.3) 0%, transparent 70%);
            transform: scale(0);
            transition: transform 0.5s;
        }
        
        .skill-item:hover::before {
            transform: scale(1);
        }
        
        .skill-item:hover {
            transform: translateY(-8px) scale(1.05) rotate(3deg);
            box-shadow: 0 15px 35px rgba(78, 205, 196, 0.6);
        }
        
        .education-item {
            margin-bottom: 25px;
            padding: 25px;
            background: linear-gradient(135deg, #f8f9fa 0%, #fff 100%);
            border-radius: 20px;
            border-right: 5px solid #45b7d1;
            box-shadow: 0 6px 20px rgba(0,0,0,0.05);
            transition: all 0.3s;
        }
        
        .education-item:hover {
            transform: translateX(-5px);
            box-shadow: 0 10px 30px rgba(69, 183, 209, 0.2);
        }
        
        .degree {
            font-size: 1.3em;
            font-weight: 700;
            color: #1a1a2e;
            margin-bottom: 10px;
        }
        
        .university {
            color: #45b7d1;
            font-weight: 600;
            margin-bottom: 8px;
        }
        
        @media (max-width: 968px) {
            .main-content {
                grid-template-columns: 1fr;
                padding: 40px 30px;
            }
            
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            .name {
                font-size: 3em;
            }
            
            .header {
                padding: 50px 30px;
            }
            
            .contact-info {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- پس‌زمینه‌های انیمیشن معماری -->
    <div class="architecture-bg">
        <div class="building"></div>
        <div class="building"></div>
        <div class="building"></div>
        <div class="building"></div>
        <div class="building"></div>
        <div class="building"></div>
        <div class="building"></div>
    </div>
    
    <div class="perspective-lines">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
    </div>
    
    <div class="floating-particles">
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
        <div class="particle"></div>
    </div>

    <div class="resume-container">
        <div class="header">
            <div class="header-content">
                <div class="photo-section">
                    <div class="photo-container">
                        <img id="profilePhoto" src="" alt="عکس پروفایل">
                        <div class="photo-placeholder">📸</div>
                    </div>
                    <label for="photoUpload" class="upload-btn">آپلود عکس</label>
                    <input type="file" id="photoUpload" accept="image/*">
                </div>
                
                <div class="name-section">
                    <h1 class="name">امیررامبد پاشاخانلو</h1>
                    <p class="title">مهندس معماری</p>
                    <p class="subtitle">دانشجوی کارشناسی ارشد مهندسی معماری</p>
                    <div class="contact-info">
                        <div class="contact-item">📧 eng.khanloo1@gmail.com</div>
                        <div class="contact-item">📱 ۰۹۹۰۶۴۰۰۲۴۴</div>
                        <div class="contact-item">📍 تهران، یوسف آباد</div>
                        <div class="contact-item">🎓 دانشجوی ارشد</div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="main-content">
            <div class="right-column">
                <div class="section">
                    <h2 class="section-title"><span class="section-icon">👤</span> درباره من</h2>
                    <p class="about-text">مهندس معمار با بیش از ۴ سال سابقه که در طی سال‌های اخیر از شروع تا پایان دو پروژه‌ی مختلف مسکونی همواره تلاش کرده‌ام با ترکیب خلاقیت، دقت فنی و مدیریت زمان، بهترین نتیجه را در طراحی و اجرا ارائه دهم. با وجود اینکه در ابتدای مسیر حرفه‌ای قرار دارم؛ با انرژی بالا، خلاقیت، پشتکار و علاقه به یادگیری و ارتقا توانایی، به‌دنبال فرصتی هستم تا در محیطی حرفه‌ای به عنوان یک معمار در بخش دفتر فنی و طراحی معماری مهارت‌هایم را توسعه دهم. هدف من این است که در کنار ارتقای توانایی‌های فردی، در پیشرفت اهداف و کیفیت پروژه‌های شرکت نیز نقش مؤثری داشته باشم و تجربه عملی ارزشمندی به دست بیاورم.</p>
                </div>
                
                <div class="section">
                    <h2 class="section-title"><span class="section-icon">💼</span> تجربیات کاری</h2>
                    
                    <div class="experience-item">
                        <h3 class="job-title">دستیار سرپرست کارگاه و ناظر جزء</h3>
                        <p class="company">🏗️ پروژه مسکونی شماره ۱ - ساخت کامل از صفر تا صد</p>
                        <p class="duration"><span>📅</span> ۲ سال | <span style="color: #4ecdc4; font-weight: 700;">حوزه: اجرا و نظارت کارگاهی</span></p>
                        <p class="description">
                            • نظارت کامل بر فرایند ساخت از پی‌کنی تا تحویل<br>
                            • هماهنگی و مدیریت تیم‌های اجرایی و پیمانکاران<br>
                            • بررسی و تایید شاپ دراوینگ و نقشه‌های اجرایی<br>
                            • کنترل کیفیت مصالح و اجرا بر اساس استانداردها<br>
                            • عکاسی و مستندسازی تمامی مراحل پروژه<br>
                            • کسب تجربه عملی از چرخه کامل ساخت
                        </p>
                    </div>
                    
                    <div class="experience-item">
                        <h3 class="job-title">دستیار سرپرست کارگاه و ناظر جزء</h3>
                        <p class="company">🏘️ پروژه مسکونی شماره ۲</p>
                        <p class="duration"><span>📅</span> ۲ سال | <span style="color: #4ecdc4; font-weight: 700;">حوزه: نظارت فنی و هماهنگی</span></p>
                        <p class="description">
                            • نظارت بر اجرای صحیح نقشه‌های معماری و سازه<br>
                            • هماهنگی با مشاوران، ناظرین و پیمانکاران<br>
                            • کنترل پیشرفت کار و گزارش‌دهی دوره‌ای<br>
                            • حل مسائل فنی و اجرایی کارگاه<br>
                            • بررسی تطبیق نقشه‌ها با اجرا
                        </p>
                    </div>
                </div>
                
                <div class="section">
                    <h2 class="section-title"><span class="section-icon">🎯</span> اهداف شغلی</h2>
                    <div class="experience-item" style="background: linear-gradient(135deg, #e8f5f3 0%, #ffffff 100%); border-right-color: #45b7d1;">
                        <p class="description" style="font-size: 1.08em;">
                            🎨 <strong style="font-size: 1.1em; color: #1a1a2e;">انتقال به حوزه طراحی و دفتر فنی</strong><br>
                            <span style="margin-right: 25px; display: inline-block; margin-top: 8px;">با ۴ سال تجربه کارگاهی و اجرایی قوی، اکنون آماده‌ام تا در بخش <strong style="color: #4ecdc4;">طراحی معماری و دفتر فنی</strong> فعالیت کنم</span><br><br>
                            
                            💡 <strong style="font-size: 1.1em; color: #1a1a2e;">ترکیب تجربه عملی و خلاقیت</strong><br>
                            <span style="margin-right: 25px; display: inline-block; margin-top: 8px;">توانایی طراحی با درک عمیق از فرایند اجرا و محدودیت‌های واقعی - طراحی قابل اجرا</span><br><br>
                            
                            🚀 <strong style="font-size: 1.1em; color: #1a1a2e;">یادگیری مستمر و رشد حرفه‌ای</strong><br>
                            <span style="margin-right: 25px; display: inline-block; margin-top: 8px;">با انرژی بالا، خلاقیت و پشتکار به دنبال رشد و توسعه مهارت‌های طراحی در محیطی حرفه‌ای</span>
                        </p>
                    </div>
                </div>
                
                <div class="section">
                    <h2 class="section-title"><span class="section-icon">⚡</span> مهارت‌های کلیدی</h2>
                    <div class="experience-item">
                        <p class="description">
                            🎨 <strong style="color: #4ecdc4; font-size: 1.1em;">طراحی معماری و دفتر فنی:</strong><br>
                            ✓ طراحی فاز یک معماری و طراحی مفهومی<br>
                            ✓ طراحی و تهیه نقشه‌های اجرایی<br>
                            ✓ طراحی نما و دیتیل‌های معماری<br>
                            ✓ آشنایی کامل با ضوابط و مقررات شهرداری<br><br>
                            
                            🖥️ <strong style="color: #45b7d1; font-size: 1.1em;">مهارت‌های فنی:</strong><br>
                            ✓ تهیه و بررسی شاپ دراوینگ<br>
                            ✓ رندرینگ و ویژوالایزیشن طراحی<br>
                            ✓ فرایند فنی و هماهنگی کارگاهی<br><br>
                            
                            🏗️ <strong style="color: #636e72; font-size: 1.1em;">تجربه اجرایی:</strong><br>
                            ✓ درک عمیق از اجرا و ساخت<br>
                            ✓ مدیریت زمان و دقت فنی<br>
                            ✓ طراحی قابل اجرا با توجه به واقعیت‌های کارگاهی
                        </p>
                    </div>
                </div>
            </div>
            
            <div class="left-column">
                <div class="section">
                    <h2 class="section-title"><span class="section-icon">🎓</span> تحصیلات</h2>
                    
                    <div class="education-item">
                        <h3 class="degree">کارشناسی ارشد</h3>
                        <p class="university">مهندسی معماری</p>
                        <p class="duration">در حال تحصیل</p>
                    </div>
                    
                    <div class="education-item">
                        <h3 class="degree">کارشناسی</h3>
                        <p class="university">مهندسی معماری</p>
                        <p class="duration">فارغ‌التحصیل</p>
                    </div>
                </div>
                
                <div class="section">
                    <h2 class="section-title"><span class="section-icon">🛠️</span> نرم‌افزارها</h2>
                    <div class="skills-grid">
                        <div class="skill-item" style="background: linear-gradient(135deg, #E41E20 0%, #C41E3A 100%);">
                            <div style="font-size: 2em; margin-bottom: 8px;">📐</div>
                            <div>AutoCAD</div>
                            <div style="font-size: 0.75em; margin-top: 5px; opacity: 0.9;">⭐⭐⭐ مسلط</div>
                        </div>
                        <div class="skill-item" style="background: linear-gradient(135deg, #0696D7 0%, #0575B8 100%);">
                            <div style="font-size: 2em; margin-bottom: 8px;">🏢</div>
                            <div>Revit</div>
                            <div style="font-size: 0.75em; margin-top: 5px; opacity: 0.9;">⭐⭐ متوسط</div>
                        </div>
                        <div class="skill-item" style="background: linear-gradient(135deg, #005F9E 0%, #004B7C 100%);">
                            <div style="font-size: 2em; margin-bottom: 8px;">📦</div>
                            <div>SketchUp</div>
                            <div style="font-size: 0.75em; margin-top: 5px; opacity: 0.9;">⭐⭐ متوسط</div>
                        </div>
                        <div class="skill-item" style="background: linear-gradient(135deg, #31A8FF 0%, #1E88E5 100%);">
                            <div style="font-size: 2em; margin-bottom: 8px;">🎨</div>
                            <div>Photoshop</div>
                            <div style="font-size: 0.75em; margin-top: 5px; opacity: 0.9;">⭐⭐ متوسط</div>
                        </div>
                    </div>
                </div>
                
                </div>
            </div>
        </div>
    </div>
</body>
</html>
<script>
const photoUpload = document.getElementById("photoUpload");
const profilePhoto = document.getElementById("profilePhoto");
const placeholder = document.querySelector(".photo-placeholder");
const uploadBtn = document.querySelector(".upload-btn");

// نمایش عکس ذخیره‌شده بعد از رفرش
window.addEventListener("load", () => {
    const savedPhoto = localStorage.getItem("profilePhoto");
    if (savedPhoto) {
        profilePhoto.src = savedPhoto;
        profilePhoto.classList.add("loaded");
        placeholder.style.display = "none";
        uploadBtn.style.display = "none";
    }
});

// آپلود عکس جدید
photoUpload.addEventListener("change", function () {
    const file = this.files[0];
    if (!file) return;

    if (file.size > 3 * 1024 * 1024) {
        alert("حجم عکس باید کمتر از ۳ مگابایت باشد");
        return;
    }

    const reader = new FileReader();
    reader.onload = function (e) {
        const imageData = e.target.result;
        profilePhoto.src = imageData;
        profilePhoto.classList.add("loaded");
        placeholder.style.display = "none";
        uploadBtn.style.display = "none";
        localStorage.setItem("profilePhoto", imageData);
    };
    reader.readAsDataURL(file);
});
</script>
