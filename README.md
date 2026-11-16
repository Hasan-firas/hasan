[hassan-medical-portfolio.html](https://github.com/user-attachments/files/34910511/hassan-medical-portfolio.html)
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>حسن فراس | Hassan Firas</title>
    <!-- خط Cairo من Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&display=swap" rel="stylesheet">
    <!-- FontAwesome للأيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --bg-color: #0b0c10;
            --card-bg: rgba(22, 27, 34, 0.75);
            --border-color: rgba(255, 222, 77, 0.2);
            --primary-accent: #FFDE4D;
            --text-main: #f0f6fc;
            --text-muted: #8b949e;
            --whatsapp-color: #25D366;
            --instagram-color: #E1306C;
            --tiktok-color: #00f2fe;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cairo', sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: var(--bg-color);
            background-image: 
                radial-gradient(circle at 50% 10%, rgba(255, 222, 77, 0.08) 0%, transparent 60%),
                radial-gradient(circle at 80% 80%, rgba(0, 242, 254, 0.04) 0%, transparent 50%);
            background-attachment: fixed;
            color: var(--text-main);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: flex-start;
            padding: 15px 12px 30px 12px;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 440px;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 16px;
            position: relative;
        }

        /* Language Switcher Fixed Container */
        .lang-switch-container {
            width: 100%;
            display: flex;
            justify-content: flex-end;
            height: 32px;
        }

        html[dir="ltr"] .lang-switch-container {
            justify-content: flex-start;
        }

        .lang-btn {
            background: rgba(255, 255, 255, 0.08);
            border: 1px solid var(--border-color);
            color: var(--primary-accent);
            padding: 5px 12px;
            border-radius: 30px;
            font-weight: 700;
            font-size: 0.8rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 6px;
            backdrop-filter: blur(10px);
            transition: all 0.2s ease;
        }

        .lang-btn:hover {
            background: rgba(255, 222, 77, 0.15);
            border-color: var(--primary-accent);
        }

        /* Profile Section */
        .profile-card {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            width: 100%;
        }

        .avatar-wrapper {
            position: relative;
            margin-bottom: 14px;
        }

        .avatar-ring {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            padding: 4px;
            background: linear-gradient(135deg, var(--primary-accent), #ff9900);
            box-shadow: 0 0 20px rgba(255, 222, 77, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .profile-img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            object-position: center 20%;
            background-color: #1a1a1a;
            border: 2px solid var(--bg-color);
        }

        .verified-badge {
            position: absolute;
            bottom: 4px;
            right: 6px;
            background: var(--primary-accent);
            color: #000;
            width: 24px;
            height: 24px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 12px;
            border: 2px solid var(--bg-color);
        }
        
        html[dir="ltr"] .verified-badge {
            right: auto;
            left: 6px;
        }

        .name {
            font-size: 1.5rem;
            font-weight: 900;
            color: #fff;
            margin-bottom: 6px;
            letter-spacing: -0.5px;
        }

        .badge-title {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            background: rgba(255, 222, 77, 0.1);
            border: 1px solid rgba(255, 222, 77, 0.3);
            color: var(--primary-accent);
            padding: 5px 14px;
            border-radius: 50px;
            font-size: 0.78rem;
            font-weight: 700;
            margin-bottom: 10px;
            text-align: center;
        }

        .bio {
            font-size: 0.88rem;
            color: var(--text-muted);
            line-height: 1.5;
            max-width: 95%;
        }

        /* Stats Section */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            width: 100%;
        }

        .stat-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            backdrop-filter: blur(12px);
            border-radius: 14px;
            padding: 12px 6px;
            text-align: center;
        }

        .stat-icon {
            font-size: 1.1rem;
            margin-bottom: 4px;
        }

        .stat-icon.insta { color: var(--instagram-color); }
        .stat-icon.tiktok { color: var(--tiktok-color); }
        .stat-icon.collab { color: var(--primary-accent); }

        .stat-number {
            font-size: 1.2rem;
            font-weight: 800;
            color: #fff;
        }

        .stat-label {
            font-size: 0.7rem;
            color: var(--text-muted);
            margin-top: 2px;
        }

        /* Section Title */
        .section-title {
            width: 100%;
            text-align: start;
            font-size: 0.9rem;
            font-weight: 700;
            color: var(--text-muted);
            margin-top: 4px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .section-title i {
            color: var(--primary-accent);
        }

        /* Collaborations Slider Section - Fixed True Infinite Loop */
        .partners-section {
            width: 100%;
            overflow: hidden;
            position: relative;
            padding: 10px 0;
        }

        .partners-section::before,
        .partners-section::after {
            content: '';
            position: absolute;
            top: 0;
            bottom: 0;
            width: 25px;
            z-index: 2;
            pointer-events: none;
        }

        .partners-section::before {
            left: 0;
            background: linear-gradient(to right, var(--bg-color), transparent);
        }

        .partners-section::after {
            right: 0;
            background: linear-gradient(to left, var(--bg-color), transparent);
        }

        .partners-track {
            display: flex;
            gap: 14px;
            width: max-content;
            animation: scrollPartners 22s linear infinite;
        }

        .partners-track:hover {
            animation-play-state: paused;
        }

        .partner-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            backdrop-filter: blur(12px);
            border-radius: 18px;
            padding: 14px;
            width: 155px;
            flex-shrink: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            gap: 10px;
            box-shadow: 0 6px 18px rgba(0,0,0,0.25);
        }

        .partner-logo-wrap {
            width: 90px;
            height: 90px;
            border-radius: 14px;
            background: #fff;
            padding: 6px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
        }

        .partner-logo {
            width: 100%;
            height: 100%;
            object-fit: contain;
            border-radius: 10px;
        }

        .partner-name {
            font-size: 0.8rem;
            font-weight: 700;
            color: #fff;
            line-height: 1.3;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        /* تصحيح اتجاه وشروط الانزلاق اللانهائي المنسجم */
        html[dir="rtl"] .partners-track {
            animation: scrollPartnersRTL 22s linear infinite;
        }

        html[dir="ltr"] .partners-track {
            animation: scrollPartnersLTR 22s linear infinite;
        }

        @keyframes scrollPartnersRTL {
            0% {
                transform: translateX(0);
            }
            100% {
                transform: translateX(calc(50% + 7px));
            }
        }

        @keyframes scrollPartnersLTR {
            0% {
                transform: translateX(0);
            }
            100% {
                transform: translateX(calc(-50% - 7px));
            }
        }

        /* Links List */
        .links-list {
            width: 100%;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .link-item {
            width: 100%;
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 14px;
            padding: 14px 16px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            text-decoration: none;
            color: #fff;
            backdrop-filter: blur(12px);
        }

        .link-left {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .link-icon {
            width: 36px;
            height: 36px;
            border-radius: 9px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.1rem;
            background: rgba(255, 255, 255, 0.05);
        }

        .link-icon.insta { color: var(--instagram-color); }
        .link-icon.tiktok { color: var(--tiktok-color); }

        .link-title {
            font-size: 0.9rem;
            font-weight: 700;
            text-align: start;
        }

        .link-handle {
            font-size: 0.72rem;
            color: var(--text-muted);
            text-align: start;
        }

        .link-arrow {
            color: var(--text-muted);
            font-size: 0.8rem;
        }

        html[dir="rtl"] .link-arrow {
            transform: rotate(0deg);
        }

        html[dir="ltr"] .link-arrow {
            transform: rotate(180deg);
        }

        /* Commercial / WhatsApp Card */
        .ad-card {
            width: 100%;
            background: linear-gradient(135deg, rgba(37, 211, 102, 0.12), rgba(22, 27, 34, 0.8));
            border: 1px solid rgba(37, 211, 102, 0.3);
            border-radius: 16px;
            padding: 16px;
            display: flex;
            flex-direction: column;
            gap: 12px;
            backdrop-filter: blur(12px);
        }

        .ad-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .ad-info {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .ad-icon {
            width: 40px;
            height: 40px;
            border-radius: 10px;
            background: rgba(37, 211, 102, 0.2);
            color: var(--whatsapp-color);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
        }

        .ad-text h3 {
            font-size: 0.92rem;
            color: #fff;
            font-weight: 700;
            text-align: start;
        }

        .ad-actions {
            display: flex;
            gap: 8px;
            width: 100%;
        }

        .btn-whatsapp {
            flex: 2;
            background: var(--whatsapp-color);
            color: #000;
            text-decoration: none;
            padding: 10px;
            border-radius: 10px;
            font-weight: 700;
            font-size: 0.85rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }

        .btn-copy {
            flex: 1;
            background: rgba(255, 255, 255, 0.08);
            border: 1px solid rgba(255, 255, 255, 0.15);
            color: #fff;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
            font-size: 0.8rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 5px;
        }

        /* Toast notification */
        .toast {
            position: fixed;
            bottom: -60px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--primary-accent);
            color: #000;
            padding: 8px 20px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 0.8rem;
            box-shadow: 0 5px 20px rgba(0,0,0,0.5);
            transition: bottom 0.3s ease;
            z-index: 1000;
        }

        .toast.show {
            bottom: 25px;
        }

        /* Footer */
        footer {
            margin-top: 10px;
            font-size: 0.72rem;
            color: var(--text-muted);
            text-align: center;
        }

        /* Premium biomedical portfolio refresh */
        :root{--bg-color:#07141b;--card-bg:rgba(14,35,43,.78);--border-color:rgba(138,220,211,.15);--primary-accent:#69e0cf;--text-main:#effaf8;--text-muted:#9bb2b4;--whatsapp-color:#35d59a}
        body{background-color:#07141b;background-image:radial-gradient(ellipse at 18% 14%,rgba(39,145,143,.18),transparent 42%),radial-gradient(ellipse at 86% 68%,rgba(32,94,120,.16),transparent 48%),linear-gradient(145deg,#07141b,#091b23 55%,#08151d);padding:28px 22px 60px;}
        .container{max-width:1080px;gap:22px;align-items:stretch}
        .lang-switch-container{height:38px}
        .lang-btn{padding:7px 16px;color:#b4fff2;border-color:rgba(105,224,207,.23);background:rgba(15,42,49,.78)}
        .profile-card{display:grid;grid-template-columns:1.08fr .92fr;grid-template-rows:auto auto auto 1fr;align-items:center;justify-items:start;text-align:start;position:relative;overflow:hidden;min-height:430px;padding:48px 50px;border:1px solid rgba(153,228,218,.16);border-radius:30px;background:linear-gradient(115deg,rgba(12,34,42,.92),rgba(9,24,32,.83));box-shadow:0 30px 90px rgba(0,0,0,.28)}
        .profile-card:before{content:"";position:absolute;inset:0;background:linear-gradient(105deg,transparent 44%,rgba(73,176,165,.035));pointer-events:none}
        .device-art{grid-column:1;grid-row:1/5;justify-self:center;position:relative;width:min(100%,430px);height:345px;display:flex;align-items:center;justify-content:center;isolation:isolate}
        .device-glow{position:absolute;width:280px;height:240px;background:rgba(64,218,203,.13);filter:blur(75px);border-radius:50%;z-index:-1;animation:glowPulse 4s ease-in-out infinite}
        .monitor-unit{position:relative;width:320px;height:244px;padding:13px 14px 16px;border:1px solid #547078;border-radius:17px;background:linear-gradient(145deg,#243b42,#10252d 56%,#0d2027);box-shadow:0 25px 50px rgba(0,0,0,.48),inset 0 1px rgba(255,255,255,.13);animation:deviceFloat 5s ease-in-out infinite;transform:perspective(800px) rotateY(-8deg) rotateX(2deg)}
        .monitor-top{height:24px;display:flex;align-items:center;justify-content:space-between;padding:0 3px 8px;color:#a9c7c8;font-size:8px;letter-spacing:1.6px}.monitor-brand{font-weight:900}.monitor-brand span{color:#6edecb}.monitor-live{display:flex;align-items:center;gap:5px;color:#7ce6c2;font-weight:700}.monitor-live i,.caption-dot{width:6px;height:6px;background:#61e2ab;border-radius:50%;box-shadow:0 0 10px #61e2ab;animation:blink 1.7s infinite}
        .monitor-screen{height:165px;border:1px solid rgba(92,205,188,.2);border-radius:8px;background:linear-gradient(145deg,#07191d,#0a2428);padding:8px 10px;box-shadow:inset 0 0 24px rgba(40,212,176,.055);overflow:hidden}.screen-meta{display:flex;justify-content:space-between;align-items:center;color:#88aaa8;font-size:8px;letter-spacing:1px}.screen-meta>span:last-child{font-size:22px;font-weight:700;color:#88f0ca;letter-spacing:0}.screen-meta small,.screen-foot small{font-size:8px;color:#7fa8a2}.ecg{width:100%;height:75px;overflow:visible;margin-top:4px}.ecg-grid{fill:none;stroke:rgba(107,210,180,.12);stroke-width:.6}.ecg-line{fill:none;stroke:#6be8b5;stroke-width:2;stroke-linecap:round;stroke-linejoin:round;stroke-dasharray:620;stroke-dashoffset:620;filter:drop-shadow(0 0 4px rgba(81,255,189,.8));animation:ecgDraw 2.8s linear infinite}
        .screen-foot{display:flex;justify-content:space-between;border-top:1px solid rgba(110,220,190,.12);padding-top:6px;color:#7fa8a2;font-size:7px;letter-spacing:.6px}.screen-foot b{font-size:12px;color:#d1fff0;margin-inline-start:3px}.monitor-controls{height:32px;display:flex;align-items:center;gap:8px;padding:7px 3px}.control-knob{width:18px;height:18px;border-radius:50%;border:3px solid #5a7176;background:radial-gradient(circle,#233c41 35%,#13262b 39%);box-shadow:0 2px 4px #071115}.control-key{width:20px;height:9px;border-radius:3px;background:#213941;border:1px solid #35525a}.monitor-stand{position:absolute;bottom:-27px;left:45%;width:38px;height:28px;background:linear-gradient(90deg,#253d43,#152b31);clip-path:polygon(24% 0,76% 0,100% 100%,0 100%)}.monitor-base{position:absolute;bottom:-31px;left:37%;width:95px;height:7px;border-radius:50%;background:#263e44;box-shadow:0 5px 16px rgba(0,0,0,.35)}
        .device-caption{position:absolute;bottom:7px;display:flex;align-items:center;gap:8px;color:#719391;font:700 8px/1 Arial,sans-serif;letter-spacing:1.5px}.caption-line{height:1px;width:45px;background:linear-gradient(90deg,rgba(105,224,207,.5),transparent)}.float-chip{position:absolute;z-index:2;display:flex;align-items:center;gap:8px;padding:10px 13px;border:1px solid rgba(132,222,211,.17);border-radius:12px;background:rgba(9,27,34,.88);box-shadow:0 12px 28px rgba(0,0,0,.22);color:#cce7e3;font-size:10px;font-weight:700;backdrop-filter:blur(12px)}.float-chip i{color:#72e4ce}.chip-a{top:45px;right:1px;animation:chipFloat 4s ease-in-out infinite}.chip-b{bottom:42px;left:-3px;animation:chipFloat 4.8s ease-in-out infinite reverse}
        .avatar-wrapper{grid-column:2;grid-row:1;margin:0 0 18px}.avatar-ring{width:58px;height:58px;padding:2px;box-shadow:0 0 0 5px rgba(105,224,207,.08)}.verified-badge{width:19px;height:19px;font-size:9px;bottom:-1px;right:-1px;border-color:#0c222a}
        html[dir="ltr"] .verified-badge{left:-1px}.name{grid-column:2;grid-row:2;font-size:clamp(2rem,4vw,3.2rem);line-height:1.2;margin:0 0 14px;letter-spacing:-1px}.badge-title{grid-column:2;grid-row:3;background:rgba(82,207,183,.09);border-color:rgba(105,224,207,.23);color:#8af0dc;margin:0 0 15px;padding:6px 13px}.bio{grid-column:2;grid-row:4;font-size:1rem;line-height:1.9;max-width:500px;color:#a8c0c0}
        .stats-grid{gap:14px}.stat-card,.partner-card,.link-item,.ad-card{background:linear-gradient(145deg,rgba(15,39,47,.88),rgba(10,28,36,.8));border-color:rgba(132,215,204,.13);box-shadow:0 12px 34px rgba(0,0,0,.12)}.stat-card{padding:18px 10px;border-radius:18px;transition:transform .25s,border-color .25s}.stat-card:hover,.link-item:hover{transform:translateY(-3px);border-color:rgba(105,224,207,.4)}.stat-icon.collab,.section-title i{color:#70e0cd}.stat-number{font-size:1.45rem}.stat-label{font-size:.76rem}.section-title{font-size:.96rem;color:#bdcece;margin-top:6px}.partners-section{padding:10px 0 16px}.partner-card{border-radius:17px}.partner-logo-wrap{background:#f9fffe}.link-item{border-radius:16px;padding:15px 18px;transition:transform .25s,border-color .25s}.link-icon{background:rgba(255,255,255,.07)}.ad-card{border-color:rgba(53,213,154,.2);background:linear-gradient(120deg,rgba(28,112,90,.16),rgba(11,31,38,.88));border-radius:19px}.btn-whatsapp{color:#062119}.toast{background:#75e3ce;color:#06201d}
        @keyframes ecgDraw{to{stroke-dashoffset:0}}@keyframes deviceFloat{0%,100%{transform:perspective(800px) rotateY(-8deg) rotateX(2deg) translateY(0)}50%{transform:perspective(800px) rotateY(-8deg) rotateX(2deg) translateY(-9px)}}@keyframes chipFloat{0%,100%{transform:translateY(0)}50%{transform:translateY(-7px)}}@keyframes glowPulse{0%,100%{opacity:.65;transform:scale(.9)}50%{opacity:1;transform:scale(1.08)}}@keyframes blink{0%,45%,100%{opacity:1}55%,90%{opacity:.28}}
        @media(max-width:720px){body{padding:18px 15px 42px}.container{gap:17px}.profile-card{grid-template-columns:1fr;grid-template-rows:auto auto auto auto auto;text-align:center;justify-items:center;padding:30px 22px 26px;min-height:unset;border-radius:24px}.device-art{grid-column:1;grid-row:1;width:100%;height:280px;margin-bottom:5px}.monitor-unit{transform:scale(.86) perspective(800px) rotateY(-8deg);transform-origin:center}.avatar-wrapper{grid-column:1;grid-row:2;margin-bottom:12px}.name{grid-column:1;grid-row:3;font-size:1.75rem;margin-bottom:12px}.badge-title{grid-column:1;grid-row:4;font-size:.72rem;margin-bottom:12px}.bio{grid-column:1;grid-row:5;font-size:.86rem;line-height:1.8}.chip-a{right:-7px;top:28px}.chip-b{left:-5px;bottom:30px;font-size:8px}.device-caption{bottom:1px}.stats-grid{gap:8px}.stat-card{padding:13px 5px;border-radius:15px}.stat-number{font-size:1.15rem}.stat-label{font-size:.63rem}.partner-card{width:145px}.partner-logo-wrap{width:82px;height:82px}}
        @media(prefers-reduced-motion:reduce){*,*::before,*::after{animation-duration:.01ms!important;animation-iteration-count:1!important;scroll-behavior:auto!important}}
        /* Scroll-following medical monitor */
        .device-art{transition:opacity .45s ease,filter .45s ease;will-change:transform,top,left}
        .device-art.is-following{position:fixed!important;z-index:30;left:max(18px,calc((100vw - 1080px)/2 - 300px));top:24vh;width:390px;height:310px;pointer-events:none;filter:drop-shadow(0 20px 42px rgba(0,0,0,.4));}
        .device-art.is-following .float-chip{opacity:.7}
        @media(max-width:1450px){.device-art.is-following{left:18px;transform-origin:top left;scale:.78}}
        @media(max-width:720px){.device-art.is-following{left:-20px;top:auto;bottom:18px;width:390px;height:250px;transform-origin:bottom left;scale:.38;opacity:.82}.device-art.is-following .device-caption,.device-art.is-following .float-chip{display:none}}
        @media(prefers-reduced-motion:reduce){.device-art{transition:none}}
    </style>
</head>
<body>

    <div class="container">

        <!-- Language Switcher Button -->
        <div class="lang-switch-container">
            <button class="lang-btn" onclick="toggleLanguage()">
                <i class="fa-solid fa-globe"></i> <span id="lang-btn-text">English</span>
            </button>
        </div>

        <!-- Profile Section -->
        <div class="profile-card">
            <div class="device-art" aria-label="Animated medical patient monitor">
                <div class="device-glow"></div>
                <div class="monitor-unit">
                    <div class="monitor-top"><span class="monitor-brand">MED<span>CORE</span></span><span class="monitor-live"><i></i> LIVE</span></div>
                    <div class="monitor-screen"><div class="screen-meta"><span>ECG · LEAD II</span><span>72 <small>BPM</small></span></div><svg class="ecg" viewBox="0 0 440 100" preserveAspectRatio="none" aria-hidden="true"><path class="ecg-grid" d="M0 20H440M0 50H440M0 80H440M55 0V100M110 0V100M165 0V100M220 0V100M275 0V100M330 0V100M385 0V100"/><path class="ecg-line" d="M0 52H75L90 49L101 52H123L136 57L149 48L163 52H178L190 52L200 17L211 87L223 36L234 52H278L291 49L302 52H324L337 58L350 47L364 52H379L391 52L401 18L412 86L424 36L435 52H450"/></svg><div class="screen-foot"><span>SpO₂ <b>98</b><small>%</small></span><span>RESP <b>16</b><small>/min</small></span><span>TEMP <b>36.8</b><small>°C</small></span></div></div>
                    <div class="monitor-controls"><span class="control-knob"></span><span class="control-key"></span><span class="control-key"></span><span class="control-key"></span><span class="control-key"></span></div>
                    <div class="monitor-stand"></div><div class="monitor-base"></div>
                </div><div class="device-caption"><span class="caption-dot"></span> BIOMEDICAL ENGINEERING <span class="caption-line"></span> 01 / 04</div>
                <span class="float-chip chip-a"><i class="fa-solid fa-heart-pulse"></i> Patient Monitoring</span><span class="float-chip chip-b"><i class="fa-solid fa-wave-square"></i> Precision in every signal</span>
            </div>
            <div class="avatar-wrapper">
                <div class="avatar-ring">
                    <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/01feaff920786e694c66829b62327d84643171dd/aa.JPEG" alt="حسن فراس" class="profile-img">
                </div>
                <div class="verified-badge">
                    <i class="fa-solid fa-check"></i>
                </div>
            </div>
            
            <h1 class="name" id="name">حسن فراس | HaSaN FiRaS</h1>
            
            <div class="badge-title">
                <i class="fa-solid fa-microscope"></i>
                <span id="badge-text">مهندس أجهزة طبية | صانع محتوى تعليمي</span>
            </div>

            <p class="bio" id="bio">
                مرحباً بكم في صفحتي الرسمية. أشارك معكم شغفي في الأجهزة الطبية والتقنية بالإضافة إلى تغطية أحدث الشراكات والتعاونات التجارية.
            </p>
        </div>

        <!-- Stats Section -->
        <div class="stats-grid">
            <div class="stat-card">
                <div class="stat-icon insta"><i class="fa-brands fa-instagram"></i></div>
                <div class="stat-number">1M+</div>
                <div class="stat-label" id="stat-insta">زيارات الإنستغرام</div>
            </div>
            <div class="stat-card">
                <div class="stat-icon tiktok"><i class="fa-brands fa-tiktok"></i></div>
                <div class="stat-number">9M+</div>
                <div class="stat-label" id="stat-tiktok">زيارات التيك توك</div>
            </div>
            <div class="stat-card">
                <div class="stat-icon collab"><i class="fa-solid fa-handshake"></i></div>
                <div class="stat-number">6+</div>
                <div class="stat-label" id="stat-collab">تعاونات تجارية</div>
            </div>
        </div>

        <!-- Strategic Collaborations Section (Continuous Loop) -->
        <div class="section-title">
            <i class="fa-solid fa-handshake-angle"></i> <span id="sec-partners">التعاونات والشراكات الاستراتيجية</span>
        </div>

        <div class="partners-section">
            <div class="partners-track" id="partnersTrack">
                <!-- Group 1 -->
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/main/%D8%B5%D9%88%D8%B1%D8%A9%206.jpg" alt="Health Expo Iraq" class="partner-logo" onerror="this.src='https://raw.githubusercontent.com/Hasan-firas/hasan/70c8c019678502d88b430431e6e0bc7ac0c2e933/%D8%B5%D9%88%D8%B1%D8%A9%201.jpg'">
                    </div>
                    <div class="partner-name" data-ar="Health Expo Iraq" data-en="Health Expo Iraq">Health Expo Iraq</div>
                </div>
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/70c8c019678502d88b430431e6e0bc7ac0c2e933/%D8%B5%D9%88%D8%B1%D8%A9%202.jpg" alt="مشروع مثقف ET" class="partner-logo">
                    </div>
                    <div class="partner-name" data-ar="مشروع مثقف ET" data-en="Educated Project (ET)">مشروع مثقف ET</div>
                </div>
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/main/%D8%B5%D9%88%D8%B1%D8%A9%204.jpg" alt="منصة التعليم العالي HEPIQ" class="partner-logo" onerror="this.src='https://raw.githubusercontent.com/Hasan-firas/hasan/70c8c019678502d88b430431e6e0bc7ac0c2e933/%D8%B5%D9%88%D8%B1%D8%A9%203.jpg'">
                    </div>
                    <div class="partner-name" data-ar="منصة التعليم العالي HEPIQ" data-en="HEPIQ Platform">منصة التعليم العالي HEPIQ</div>
                </div>
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/main/%D8%B5%D9%88%D8%B1%D8%A9%203.jpg" alt="رابطة رواد هندسة الطب الحياتي" class="partner-logo" onerror="this.src='https://raw.githubusercontent.com/Hasan-firas/hasan/70c8c019678502d88b430431e6e0bc7ac0c2e933/%D8%B5%D9%88%D8%B1%D8%A9%204.jpg'">
                    </div>
                    <div class="partner-name" data-ar="رابطة رواد هندسة الطب الحياتي" data-en="Pioneers of B.M.E">رابطة رواد هندسة الطب الحياتي</div>
                </div>
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/70c8c019678502d88b430431e6e0bc7ac0c2e933/%D8%B5%D9%88%D8%B1%D8%A9%205.jpg" alt="زوين للكتب الهندسية" class="partner-logo">
                    </div>
                    <div class="partner-name" data-ar="زوين للكتب الهندسية" data-en="Zowin Engineering Books">زوين للكتب الهندسية</div>
                </div>
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/f0c026813395ee6edb5aca8df77ed751d8545fdb/%D8%B5%D9%88%D8%B1%D8%A9%207.jpg" alt="شركة QI" class="partner-logo">
                    </div>
                    <div class="partner-name" data-ar="شركة كي كارد (QI)" data-en="Qi Card Company">شركة كي كارد (QI)</div>
                </div>

                <!-- Group 2 Duplicate for Loop -->
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/main/%D8%B5%D9%88%D8%B1%D8%A9%206.jpg" alt="Health Expo Iraq" class="partner-logo">
                    </div>
                    <div class="partner-name" data-ar="Health Expo Iraq" data-en="Health Expo Iraq">Health Expo Iraq</div>
                </div>
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/70c8c019678502d88b430431e6e0bc7ac0c2e933/%D8%B5%D9%88%D8%B1%D8%A9%202.jpg" alt="مشروع مثقف ET" class="partner-logo">
                    </div>
                    <div class="partner-name" data-ar="مشروع مثقف ET" data-en="Educated Project (ET)">مشروع مثقف ET</div>
                </div>
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/main/%D8%B5%D9%88%D8%B1%D8%A9%204.jpg" alt="منصة التعليم العالي HEPIQ" class="partner-logo">
                    </div>
                    <div class="partner-name" data-ar="منصة التعليم العالي HEPIQ" data-en="HEPIQ Platform">منصة التعليم العالي HEPIQ</div>
                </div>
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/main/%D8%B5%D9%88%D8%B1%D8%A9%203.jpg" alt="رابطة رواد هندسة الطب الحياتي" class="partner-logo">
                    </div>
                    <div class="partner-name" data-ar="رابطة رواد هندسة الطب الحياتي" data-en="Pioneers of B.M.E">رابطة رواد هندسة الطب الحياتي</div>
                </div>
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/70c8c019678502d88b430431e6e0bc7ac0c2e933/%D8%B5%D9%88%D8%B1%D8%A9%205.jpg" alt="زوين للكتب الهندسية" class="partner-logo">
                    </div>
                    <div class="partner-name" data-ar="زوين للكتب الهندسية" data-en="Zowin Engineering Books">زوين للكتب الهندسية</div>
                </div>
                <div class="partner-card">
                    <div class="partner-logo-wrap">
                        <img src="https://raw.githubusercontent.com/Hasan-firas/hasan/f0c026813395ee6edb5aca8df77ed751d8545fdb/%D8%B5%D9%88%D8%B1%D8%A9%207.jpg" alt="شركة QI" class="partner-logo">
                    </div>
                    <div class="partner-name" data-ar="شركة كي كارد (QI)" data-en="Qi Card Company">شركة كي كارد (QI)</div>
                </div>
            </div>
        </div>

        <!-- Social Links Section -->
        <div class="section-title">
            <i class="fa-solid fa-globe"></i> <span id="sec-social">حساباتي الرسمية</span>
        </div>

        <div class="links-list">
            <!-- Instagram -->
            <a href="https://instagram.com/z29u" target="_blank" class="link-item">
                <div class="link-left">
                    <div class="link-icon insta">
                        <i class="fa-brands fa-instagram"></i>
                    </div>
                    <div>
                        <div class="link-title" id="title-insta">حساب الإنستغرام</div>
                        <div class="link-handle">@z29u</div>
                    </div>
                </div>
                <div class="link-arrow">
                    <i class="fa-solid fa-chevron-left"></i>
                </div>
            </a>

            <!-- TikTok -->
            <a href="https://www.tiktok.com/@1_6c" target="_blank" class="link-item">
                <div class="link-left">
                    <div class="link-icon tiktok">
                        <i class="fa-brands fa-tiktok"></i>
                    </div>
                    <div>
                        <div class="link-title" id="title-tiktok">حساب التيك توك</div>
                        <div class="link-handle">@1_6c</div>
                    </div>
                </div>
                <div class="link-arrow">
                    <i class="fa-solid fa-chevron-left"></i>
                </div>
            </a>
        </div>

        <!-- Commercial / Ad Section (Moved to the bottom) -->
        <div class="section-title">
            <i class="fa-solid fa-briefcase"></i> <span id="sec-commercial">الإعلانات والتعاون التجاري</span>
        </div>

        <div class="ad-card">
            <div class="ad-header">
                <div class="ad-info">
                    <div class="ad-icon">
                        <i class="fa-brands fa-whatsapp"></i>
                    </div>
                    <div class="ad-text">
                        <h3 id="wa-title">مباشر واتساب للأعمال</h3>
                    </div>
                </div>
            </div>
            <div class="ad-actions">
                <a href="https://wa.me/9647835552957" target="_blank" class="btn-whatsapp">
                    <i class="fa-solid fa-paper-plane"></i> <span id="btn-chat">مراسلة</span>
                </a>
                <button class="btn-copy" onclick="copyNumber('+9647835552957')">
                    <i class="fa-regular fa-copy"></i> <span id="btn-copy-text">نسخ</span>
                </button>
            </div>
        </div>

        <!-- Footer -->
        <footer id="footer">
            © HaSaN FiRaS | جميع الحقوق محفوظة
        </footer>

    </div>

    <!-- Toast Component -->
    <div id="toast" class="toast">تم نسخ الرقم بنجاح!</div>

    <script>
        let currentLang = 'ar';

        const translations = {
            ar: {
                langBtn: "English",
                name: "حسن فراس | HaSaN FiRaS",
                badge: "مهندس أجهزة طبية | صانع محتوى تعليمي",
                bio: "مرحباً بكم في صفحتي الرسمية. أشارك معكم شغفي في الأجهزة الطبية والتقنية بالإضافة إلى تغطية أحدث الشراكات والتعاونات التجارية.",
                statInsta: "زيارات الإنستغرام",
                statTiktok: "زيارات التيك توك",
                statCollab: "تعاونات تجارية",
                secCommercial: "الإعلانات والتعاون التجاري",
                secPartners: "التعاونات والشراكات الاستراتيجية",
                waTitle: "مباشر واتساب للأعمال",
                btnChat: "مراسلة",
                btnCopy: "نسخ",
                secSocial: "حساباتي الرسمية",
                titleInsta: "حساب الإنستغرام",
                titleTiktok: "حساب التيك توك",
                footer: "© HaSaN FiRaS | جميع الحقوق محفوظة",
                toastMsg: "تم نسخ الرقم بنجاح!"
            },
            en: {
                langBtn: "عربي",
                name: "HaSaN FiRaS | حسن فراس",
                badge: "Medical instrumentation engineer | Educational Creator",
                bio: "Welcome to my official page. Sharing my passion for Medical instrumentation, technology, and covering commercial partnerships.",
                statInsta: "Instagram Visits",
                statTiktok: "TikTok Visits",
                statCollab: "Brand Collaborations",
                secCommercial: "Ads & Business Inquiries",
                secPartners: "Strategic Collaborations & Partners",
                waTitle: "WhatsApp Business Direct",
                btnChat: "Message",
                btnCopy: "Copy",
                secSocial: "Official Accounts",
                titleInsta: "Instagram Profile",
                titleTiktok: "TikTok Profile",
                footer: "© HaSaN FiRaS | All Rights Reserved",
                toastMsg: "Number copied successfully!"
            }
        };

        function toggleLanguage() {
            currentLang = currentLang === 'ar' ? 'en' : 'ar';
            const t = translations[currentLang];

            document.documentElement.setAttribute('lang', currentLang);
            document.documentElement.setAttribute('dir', currentLang === 'ar' ? 'rtl' : 'ltr');

            document.getElementById('lang-btn-text').innerText = t.langBtn;
            document.getElementById('name').innerText = t.name;
            document.getElementById('badge-text').innerText = t.badge;
            document.getElementById('bio').innerText = t.bio;
            document.getElementById('stat-insta').innerText = t.statInsta;
            document.getElementById('stat-tiktok').innerText = t.statTiktok;
            document.getElementById('stat-collab').innerText = t.statCollab;
            document.getElementById('sec-commercial').innerText = t.secCommercial;
            document.getElementById('sec-partners').innerText = t.secPartners;
            document.getElementById('wa-title').innerText = t.waTitle;
            document.getElementById('btn-chat').innerText = t.btnChat;
            document.getElementById('btn-copy-text').innerText = t.btnCopy;
            document.getElementById('sec-social').innerText = t.secSocial;
            document.getElementById('title-insta').innerText = t.titleInsta;
            document.getElementById('title-tiktok').innerText = t.titleTiktok;
            document.getElementById('footer').innerText = t.footer;
            document.getElementById('toast').innerText = t.toastMsg;

            const partnerNames = document.querySelectorAll('.partner-name');
            partnerNames.forEach(el => {
                el.innerText = el.getAttribute(`data-${currentLang}`);
            });
        }

        function copyNumber(text) {
            navigator.clipboard.writeText(text).then(() => {
                const toast = document.getElementById('toast');
                toast.classList.add('show');
                setTimeout(() => {
                    toast.classList.remove('show');
                }, 2000);
            });
        }

        // Let the medical monitor accompany the reader while scrolling.
        (() => {
            const device = document.querySelector('.device-art');
            if (!device) return;
            let currentY = 0, targetY = 0, ticking = false;
            const update = () => {
                targetY = window.scrollY;
                if (!ticking) {
                    ticking = true;
                    requestAnimationFrame(function animate() {
                        currentY += (targetY - currentY) * 0.12;
                        const active = currentY > 240;
                        device.classList.toggle('is-following', active);
                        if (active) {
                            const drift = Math.min(currentY * 0.035, 110) + Math.sin(currentY / 520) * 10;
                            const tilt = Math.sin(currentY / 700) * 2.5;
                            device.style.margin = '0';
                            device.style.transform = `translate3d(0, ${drift}px, 0) rotate(${tilt}deg)`;
                        } else {
                            device.style.transform = '';
                            device.style.margin = '';
                        }
                        if (Math.abs(targetY - currentY) > 0.5) requestAnimationFrame(animate);
                        else ticking = false;
                    });
                }
            };
            window.addEventListener('scroll', update, { passive: true });
            window.addEventListener('resize', update, { passive: true });
        })();
    </script>
</body>
</html>




