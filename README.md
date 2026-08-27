<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>الابتلاء العظيم — قصة عن الأمل والصبر</title>
    <meta name="description" content="تجربة قصصية تفاعلية عن الصبر والأمل والاستمرار — رحلة من اليأس إلى الطمأنينة." />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,400;0,700;1,400&family=Tajawal:wght@300;400;500;700;800&family=Aref+Ruqaa:wght@400;700&display=swap"
      rel="stylesheet"
    />
    <style>
        /* ===== CSS Variables & Reset ===== */
        :root {
            --font-display: 'Amiri', 'Aref Ruqaa', serif;
            --font-body: 'Tajawal', sans-serif;
            --font-quote: 'Aref Ruqaa', serif;
            --color-dark-0: #080810;
            --color-dark-1: #0d0d1a;
            --color-dark-2: #121222;
            --color-dark-3: #1a1a30;
            --color-dark-4: #252540;
            --color-mid-1: #3a3a5e;
            --color-mid-2: #4e4e72;
            --color-mid-3: #6b6b8e;
            --color-light-1: #9a9ab4;
            --color-warm-1: #d4cbb8;
            --color-warm-2: #e8e0d4;
            --color-warm-3: #f5f0e8;
            --color-gold: #d4a853;
            --color-gold-light: #e8c987;
            --color-text-light: #f0ede8;
            --color-text-dark: #1a1a2e;
            --transition-smooth: cubic-bezier(0.4, 0, 0.2, 1);
            --transition-slow: cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            font-family: var(--font-body);
            background-color: var(--color-dark-0);
            color: var(--color-text-light);
            overflow-x: hidden;
            line-height: 1.8;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            transition: background-color 0.6s var(--transition-smooth);
        }

        /* ===== Scrollbar ===== */
        ::-webkit-scrollbar {
            width: 6px;
        }
        ::-webkit-scrollbar-track {
            background: transparent;
        }
        ::-webkit-scrollbar-thumb {
            background: rgba(255, 255, 255, 0.15);
            border-radius: 3px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: rgba(255, 255, 255, 0.25);
        }

        /* ===== Selection ===== */
        ::selection {
            background: var(--color-gold);
            color: var(--color-dark-0);
        }

        /* ===== Typography ===== */
        .font-display {
            font-family: var(--font-display);
        }
        .font-quote {
            font-family: var(--font-quote);
        }
        .font-body {
            font-family: var(--font-body);
        }

        /* ===== Animations ===== */
        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(24px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-16px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        @keyframes slowZoom {
            from {
                transform: scale(1);
            }
            to {
                transform: scale(1.06);
            }
        }
        @keyframes pulseGlow {
            0%,
            100% {
                opacity: 0.3;
            }
            50% {
                opacity: 0.6;
            }
        }
        @keyframes floatParticle {
            0%,
            100% {
                transform: translateY(0) translateX(0);
                opacity: 0.2;
            }
            25% {
                transform: translateY(-20px) translateX(10px);
                opacity: 0.5;
            }
            50% {
                transform: translateY(-35px) translateX(-5px);
                opacity: 0.35;
            }
            75% {
                transform: translateY(-15px) translateX(-15px);
                opacity: 0.5;
            }
        }
        @keyframes shimmer {
            0% {
                background-position: -200% center;
            }
            100% {
                background-position: 200% center;
            }
        }

        .animate-fadeIn {
            animation: fadeIn 0.6s var(--transition-smooth) forwards;
        }
        .animate-fadeInUp {
            animation: fadeInUp 0.7s var(--transition-smooth) forwards;
        }
        .animate-fadeInDown {
            animation: fadeInDown 0.5s var(--transition-smooth) forwards;
        }
        .animate-slowZoom {
            animation: slowZoom 20s ease-in-out infinite alternate;
        }
        .animate-pulseGlow {
            animation: pulseGlow 4s ease-in-out infinite;
        }
        .animate-floatParticle {
            animation: floatParticle 8s ease-in-out infinite;
        }

        /* ===== Scroll Reveal ===== */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s var(--transition-smooth), transform 0.8s var(--transition-smooth);
            transition-delay: var(--reveal-delay, 0ms);
        }
        .reveal.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .reveal-fade-only {
            opacity: 0;
            transition: opacity 1s var(--transition-smooth);
            transition-delay: var(--reveal-delay, 0ms);
        }
        .reveal-fade-only.visible {
            opacity: 1;
        }

        /* ===== Opening / Closing Overlays ===== */
        .overlay-screen {
            position: fixed;
            inset: 0;
            z-index: 1000;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            background: var(--color-dark-0);
            transition: opacity 0.8s var(--transition-smooth), visibility 0.8s var(--transition-smooth);
            opacity: 1;
            visibility: visible;
        }
        .overlay-screen.hidden-overlay {
            opacity: 0;
            visibility: hidden;
            pointer-events: none;
        }

        /* ===== Particles ===== */
        .particle {
            position: absolute;
            border-radius: 50%;
            pointer-events: none;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.6) 0%, rgba(255, 255, 255, 0) 70%);
            filter: blur(1px);
        }

        /* ===== Input Styles ===== */
        .story-input {
            width: 100%;
            max-width: 520px;
            padding: 1rem 1.5rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.15);
            border-radius: 12px;
            color: var(--color-text-light);
            font-family: var(--font-body);
            font-size: 1rem;
            transition: all 0.4s var(--transition-smooth);
            resize: vertical;
            min-height: 100px;
        }
        .story-input:focus {
            outline: none;
            border-color: var(--color-gold);
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 0 30px rgba(212, 168, 83, 0.15);
        }
        .story-input::placeholder {
            color: rgba(255, 255, 255, 0.35);
        }

        /* ===== Button Styles ===== */
        .btn-primary {
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            padding: 0.85rem 2.4rem;
            background: var(--color-gold);
            color: var(--color-dark-0);
            font-family: var(--font-body);
            font-weight: 700;
            font-size: 1.05rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.4s var(--transition-smooth);
            text-decoration: none;
            letter-spacing: 0.02em;
        }
        .btn-primary:hover {
            background: var(--color-gold-light);
            transform: translateY(-2px);
            box-shadow: 0 8px 30px rgba(212, 168, 83, 0.3);
        }
        .btn-primary:active {
            transform: translateY(0);
            box-shadow: 0 4px 15px rgba(212, 168, 83, 0.2);
        }

        .btn-secondary {
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            padding: 0.85rem 2.4rem;
            background: transparent;
            color: var(--color-text-light);
            font-family: var(--font-body);
            font-weight: 500;
            font-size: 1.05rem;
            border: 1.5px solid rgba(255, 255, 255, 0.3);
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.4s var(--transition-smooth);
            text-decoration: none;
            letter-spacing: 0.02em;
        }
        .btn-secondary:hover {
            border-color: var(--color-gold);
            color: var(--color-gold);
            background: rgba(212, 168, 83, 0.05);
            transform: translateY(-2px);
        }

        /* ===== Chapter Container ===== */
        .chapter-section {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 3rem 1.5rem;
            position: relative;
            transition: background-color 0.8s var(--transition-smooth);
        }

        /* ===== Gradient Overlays ===== */
        .vignette {
            position: absolute;
            inset: 0;
            pointer-events: none;
            background: radial-gradient(ellipse at center, transparent 30%, rgba(0, 0, 0, 0.5) 100%);
            transition: opacity 0.8s var(--transition-smooth);
        }

        /* ===== Background Layer ===== */
        .bg-layer {
            position: fixed;
            inset: 0;
            z-index: 0;
            pointer-events: none;
            transition: background-color 0.7s var(--transition-smooth);
        }

        /* ===== Content Layering ===== */
        .content-layer {
            position: relative;
            z-index: 10;
        }

        /* ===== Quote Block ===== */
        .quote-block {
            text-align: center;
            padding: 4rem 1.5rem;
            max-width: 680px;
            margin: 0 auto;
        }

        /* ===== Mobile Menu ===== */
        .mobile-menu {
            position: fixed;
            inset: 0;
            z-index: 900;
            background: rgba(8, 8, 16, 0.97);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 1.5rem;
            transition: opacity 0.5s var(--transition-smooth), visibility 0.5s var(--transition-smooth);
            opacity: 0;
            visibility: hidden;
        }
        .mobile-menu.open {
            opacity: 1;
            visibility: visible;
        }

        /* ===== Smooth scroll container ===== */
        .story-scroll-container {
            position: relative;
            z-index: 5;
        }

        /* ===== Responsive Typography ===== */
        @media (max-width: 768px) {
            html {
                font-size: 15px;
            }
            .chapter-section {
                padding: 2.5rem 1.25rem;
                min-height: 80vh;
            }
            .quote-block {
                padding: 3rem 1.25rem;
            }
            .btn-primary,
            .btn-secondary {
                padding: 0.75rem 1.8rem;
                font-size: 0.95rem;
            }
            .story-input {
                font-size: 0.9rem;
                padding: 0.85rem 1.2rem;
                min-height: 80px;
            }
        }
        @media (max-width: 480px) {
            html {
                font-size: 14px;
            }
            .chapter-section {
                padding: 2rem 1rem;
            }
        }
        @media (min-width: 1200px) {
            html {
                font-size: 18px;
            }
            .chapter-section {
                padding: 4rem 2rem;
            }
        }
    </style>
</head>
<body>
    <div id="root"></div>
    <script type="module">
        import React from 'react';
        import { createRoot } from 'react-dom/client';
        import { useState, useEffect, useRef, useCallback, useMemo } from 'react';
        import {
            Menu, X, Play, Pause, ChevronDown, BookOpen, Heart, Sparkles,
            MessageCircle, ArrowRight, ArrowLeft, Sun, Moon, Star, Cloud,
            CloudRain, CloudSun, Wind, Music, BookMarked, Feather, PenLine,
            CheckCircle2, RotateCcw, Share2, Download, Copy, Info, Shield, Mail
        } from 'lucide-react';

        // ===== STORY DATA =====
        const STORY_TITLE = 'الابتلاء العظيم';
        const OPENING_QUOTE = 'ليست كل الطرق سهلة… لكن بعض الطرق تصنع منك إنسانًا أقوى.';

        const storyChapters = [{
            id: 'chapter-1',
            title: 'الفصل الأول — البداية',
            icon: Cloud,
            tone: 'dark',
            paragraphs: [
                'في بعض الأيام، لا يحدث شيء سيئ بشكل واضح… لكنك مع ذلك تشعر بثقل لا تستطيع تفسيره.',
                'تستيقظ في الصباح، وتمر الساعات بطيئة. تفعل ما عليك فعله، لكن قلبك ليس حاضرًا.',
                'تنظر إلى نفسك في المرآة وترى شخصًا تحاول أن تتعرف عليه من جديد. الابتسامة صارت أثقل، والأفكار صارت أسرع من قدرتك على اللحاق بها.',
                'تشعر وكأنك تنظر إلى حياتك من خلف زجاج. كل شيء يتحرك حولك، لكنك عالق في مكان لا يشبهك.'
            ]
        }, {
            id: 'chapter-2',
            title: 'الفصل الثاني — لماذا أنا؟',
            icon: CloudRain,
            tone: 'dark',
            paragraphs: [
                '"لماذا يحدث هذا لي؟" سؤال يتكرر في رأسك. تنظر إلى الآخرين وتتساءل: لماذا تبدو حياتهم أسهل؟ لماذا يبدو الطريق أمامهم واضحًا بينما أنت تتلمس خطواتك في العتمة؟',
                'الخوف من المستقبل يطرق بابك كل ليلة. ماذا لو استمر هذا الشعور؟ ماذا لو لم أجد إجابة؟ ماذا لو…',
                'أنت لا تفهم كل شيء الآن. وهذا طبيعي تمامًا. ليس عليك أن تملك كل الإجابات. ليس عليك أن تعرف لماذا حدث كل هذا.',
                'الحيرة ليست ضعفًا. الحيرة إشارة إلى أنك إنسان يبحث عن معنى، وأن قلبك ما زال حيًا رغم كل شيء.'
            ]
        }, {
            id: 'chapter-3',
            title: 'الفصل الثالث — الصبر',
            icon: CloudSun,
            tone: 'transition',
            paragraphs: [
                'الصبر ليس أن تتوقف عن الشعور. الصبر ليس أن تتظاهر بأنك بخير بينما أنت منهك من الداخل.',
                'الصبر أن تستمر يومًا آخر رغم أنك لا ترى النهاية. أن تعطي نفسك وقتًا. أن تتقبل أن بعض الأشياء تحتاج وقتًا لتلتئم.',
                'الصبر أن تطلب المساعدة عندما تحتاجها. أن تخبر شخصًا تثق به أنك لست بخير، دون أن تشعر أن هذا اعتراف بالهزيمة.',
                'الصبر أن تؤمن بأن الوضع الحالي يمكن أن يتغير. ليس لأنك متفائل ساذج، بل لأنك تعرف أن كل شيء في هذه الحياة له وقت، ولكل شيء نهاية.',
                'الصبر رحلة وليس لحظة واحدة. إنه الطريق الذي يمشي عليه من يرفض أن يستسلم رغم ثقل الخطوات.'
            ]
        }, {
            id: 'chapter-4',
            title: 'الفصل الرابع — نافذة صغيرة',
            icon: Sun,
            tone: 'transition',
            paragraphs: [
                'ثم في يوم من الأيام، لاحظت شيئًا صغيرًا.',
                'شخص وقف بجانبك دون أن تطلب. لحظة هدوء في يوم مزدحم. فرصة جديدة لم تكن تتوقعها. إنجاز صغير شعرت به بفرح لم تعرفه منذ وقت.',
                'يوم كان أفضل قليلًا من اليوم السابق. نومة أعمق. ضحكة صادقة فاجأتك وأنت لا تنوي.',
                'الأمل لا يأتي دائمًا كشيء ضخم. أحيانًا يبدأ كشيء صغير جدًا.',
                'نافذة صغيرة في جدار مظلم. لكنها كافية لتمرير ضوء.'
            ]
        }, {
            id: 'chapter-5',
            title: 'الفصل الخامس — لم تنتهِ القصة',
            icon: Wind,
            tone: 'light',
            paragraphs: [
                'أدركت أن المرحلة الصعبة كانت فصلًا من حياتك، وليست حياتك كلها.',
                'لقد مررت بأيام شعرت فيها أن لا شيء سيتغير. لكن ها أنت هنا، تقرأ هذه الكلمات. ما زلت تكمل.',
                'قد لا تعرف ما سيحدث غدًا. قد لا تعرف إلى أين يقودك هذا الطريق. لكنك لا تحتاج إلى معرفة النهاية حتى تكمل الطريق.',
                'ما زال هناك فصل لم يُكتب. صفحات بيضاء تنتظرك. وقرارات لم تتخذها بعد. وأيام ستأتي لا تشبه أيامك التي مضت.',
                'قصتك لم تكتمل. وأنت لا تزال تمسك القلم.'
            ]
        }, {
            id: 'chapter-6',
            title: 'الفصل الأخير — الأمل',
            icon: Sparkles,
            tone: 'light',
            paragraphs: [
                'أحيانًا يكون الأمل مجرد أن تكمل.',
                'أن تخطو خطوة أخرى رغم أنك متعب. أن تفتح عينيك في الصباح وتقول: سأحاول اليوم. أن تؤمن أن غدًا قد يكون مختلفًا.',
                'إذا كنت تمر بوقت صعب، فلا تجعل يومًا صعبًا يقنعك أن كل أيامك ستكون كذلك.',
                'خذ يومك خطوة بخطوة. لا تفكر في كل الطريق، فقط في الخطوة القادمة. ثم التي تليها.',
                'الأمل ليس وعدًا بأن كل شيء سيكون مثاليًا. الأمل هو إيمانك بأن الأمر يستحق المحاولة. أنك تستحق المحاولة.'
            ]
        }];

        const quotes = [
            'ليس عليك أن ترى الطريق كاملًا حتى تخطو الخطوة التالية.',
            'بعض الأيام تحتاج منك فقط أن تكملها.',
            'الأمل قد يبدأ صغيرًا… لكنه يكفي ليغيّر اتجاهك.'
        ];

        const interactiveQuestions = [
            { id: 'q1', chapterAfter: 'chapter-2', label: 'ما الشيء الذي تتمنى أن يتحسن؟', placeholder: 'اكتب هنا… أو اتركه فارغًا', storageKey: 'trial-great-q1' },
            { id: 'q2', chapterAfter: 'chapter-5', label: 'ما الذي تريد أن تقوله لنفسك اليوم؟', placeholder: 'اكتب رسالة قصيرة لنفسك…', storageKey: 'trial-great-q2' }
        ];

        const finalMessagePrompt = {
            id: 'final',
            label: 'اكتب رسالة لنفسك تقرأها بعد فترة.',
            placeholder: 'اكتب رسالة لنفسك… ستحفظ في متصفحك فقط',
            storageKey: 'trial-great-final-message'
        };

        // ===== COLOR INTERPOLATION UTILITIES =====
        function hexToRgb(hex) {
            const h = hex.replace('#', '');
            return [
                parseInt(h.substring(0, 2), 16),
                parseInt(h.substring(2, 4), 16),
                parseInt(h.substring(4, 6), 16)
            ];
        }

        function rgbToHex(r, g, b) {
            return '#' + [r, g, b].map(x => Math.max(0, Math.min(255, Math.round(x))).toString(16).padStart(2, '0')).join('');
        }

        function lerpColor(color1, color2, t) {
            const rgb1 = hexToRgb(color1);
            const rgb2 = hexToRgb(color2);
            const r = rgb1[0] + (rgb2[0] - rgb1[0]) * t;
            const g = rgb1[1] + (rgb2[1] - rgb1[1]) * t;
            const b = rgb1[2] + (rgb2[2] - rgb1[2]) * t;
            return rgbToHex(r, g, b);
        }

        const colorStops = [
            { progress: 0.0, color: '#080810' },
            { progress: 0.08, color: '#0d0d1a' },
            { progress: 0.18, color: '#121222' },
            { progress: 0.30, color: '#1a1a30' },
            { progress: 0.42, color: '#252540' },
            { progress: 0.55, color: '#3a3a5e' },
            { progress: 0.68, color: '#4e4e72' },
            { progress: 0.80, color: '#6b6b8e' },
            { progress: 0.90, color: '#d4cbb8' },
            { progress: 1.0, color: '#f5f0e8' }
        ];

        function getBackgroundColor(progress) {
            const clamped = Math.max(0, Math.min(1, progress));
            for (let i = 0; i < colorStops.length - 1; i++) {
                const a = colorStops[i];
                const b = colorStops[i + 1];
                if (clamped >= a.progress && clamped <= b.progress) {
                    const range = b.progress - a.progress;
                    const t = range === 0 ? 0 : (clamped - a.progress) / range;
                    return lerpColor(a.color, b.color, t);
                }
            }
            return colorStops[colorStops.length - 1].color;
        }

        function getTextColor(progress) {
            return progress > 0.75 ? '#1a1a2e' : '#f0ede8';
        }

        function getMutedTextColor(progress) {
            return progress > 0.75 ? 'rgba(26, 26, 46, 0.6)' : 'rgba(240, 237, 232, 0.6)';
        }

        // ===== HOOKS =====
        function useScrollProgress(ref) {
            const [progress, setProgress] = useState(0);
            const [scrollY, setScrollY] = useState(0);

            useEffect(() => {
                const handleScroll = () => {
                    const el = ref.current;
                    if (!el) return;
                    const rect = el.getBoundingClientRect();
                    const windowHeight = window.innerHeight;
                    const totalScrollable = el.scrollHeight - windowHeight;
                    const scrolled = -rect.top;
                    const newProgress = totalScrollable > 0 ? Math.max(0, Math.min(1, scrolled / totalScrollable)) : 0;
                    setProgress(newProgress);
                    setScrollY(scrolled);
                };
                handleScroll();
                window.addEventListener('scroll', handleScroll, { passive: true });
                window.addEventListener('resize', handleScroll, { passive: true });
                return () => {
                    window.removeEventListener('scroll', handleScroll);
                    window.removeEventListener('resize', handleScroll);
                };
            }, [ref]);
            return { progress, scrollY };
        }

        function useScrollReveal() {
            const elementsRef = useRef([]);

            useEffect(() => {
                const observer = new IntersectionObserver(
                    (entries) => {
                        entries.forEach((entry) => {
                            if (entry.isIntersecting) {
                                entry.target.classList.add('visible');
                            }
                        });
                    }, { threshold: 0.15, rootMargin: '0px 0px -40px 0px' }
                );
                const elements = document.querySelectorAll('.reveal, .reveal-fade-only');
                elements.forEach((el) => observer.observe(el));
                return () => {
                    elements.forEach((el) => observer.unobserve(el));
                };
            }, []);

            const setDelay = useCallback((index) => ({ '--reveal-delay': `${index * 120}ms` }), []);
            return { setDelay };
        }

        function useLocalStorage(key, initialValue = '') {
            const [value, setValue] = useState(() => {
                try {
                    return localStorage.getItem(key) || initialValue;
                } catch {
                    return initialValue;
                }
            });
            const setStoredValue = useCallback((newValue) => {
                setValue(newValue);
                try {
                    if (newValue) {
                        localStorage.setItem(key, newValue);
                    } else {
                        localStorage.removeItem(key);
                    }
                } catch {}
            }, [key]);
            return [value, setStoredValue];
        }

        // ===== COMPONENTS =====
        function Particles({ count = 18 }) {
            const particles = useMemo(() => {
                return Array.from({ length: count }, (_, i) => ({
                    id: i,
                    x: Math.random() * 100,
                    y: Math.random() * 100,
                    size: Math.random() * 3 + 1,
                    delay: Math.random() * 8,
                    duration: Math.random() * 6 + 6
                }));
            }, [count]);
            return (
                <div className="absolute inset-0 overflow-hidden pointer-events-none" style={{ zIndex: 1 }}>
                    {particles.map((p) => (
                        <div
                            key={p.id}
                            className="particle animate-floatParticle"
                            style={{
                                left: `${p.x}%`,
                                top: `${p.y}%`,
                                width: `${p.size}px`,
                                height: `${p.size}px`,
                                animationDelay: `${p.delay}s`,
                                animationDuration: `${p.duration}s`
                            }}
                        />
                    ))}
                </div>
            );
        }

        function Navbar({ onStartStory, currentProgress }) {
            const [mobileMenuOpen, setMobileMenuOpen] = useState(false);
            const [scrolled, setScrolled] = useState(false);
            const isLight = currentProgress > 0.7;
            const textColor = isLight ? '#1a1a2e' : '#f0ede8';
            const bgOpacity = scrolled ? (isLight ? '0.95' : '0.85') : '0';

            useEffect(() => {
                const handleScroll = () => setScrolled(window.scrollY > 40);
                handleScroll();
                window.addEventListener('scroll', handleScroll, { passive: true });
                return () => window.removeEventListener('scroll', handleScroll);
            }, []);

            const navLinks = [
                { label: 'البداية', href: '#hero' },
                { label: 'القصة', href: '#story' },
                { label: 'الفصول', href: '#chapters-overview' },
                { label: 'عن المشروع', href: '#about' }
            ];

            return (
                <>
                    <header
                        className="fixed top-0 left-0 right-0 z-50 transition-all duration-500"
                        style={{
                            backgroundColor: `rgba(${isLight ? '245, 240, 232' : '8, 8, 16'}, ${bgOpacity})`,
                            backdropFilter: scrolled ? 'blur(12px)' : 'none',
                            borderBottom: scrolled ? `1px solid rgba(${isLight ? '26,26,46' : '255,255,255'}, 0.08)` : 'none'
                        }}
                    >
                        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                            <div className="flex items-center justify-between h-16 md:h-20">
                                <button
                                    onClick={() => window.scrollTo({ top: 0, behavior: 'smooth' })}
                                    className="font-display font-bold text-xl md:text-2xl transition-colors duration-300"
                                    style={{ color: textColor }}
                                >
                                    {STORY_TITLE}
                                </button>

                                {/* Desktop Nav */}
                                <nav className="hidden md:flex items-center gap-6 lg:gap-8">
                                    {navLinks.map((link) => (
                                        <a
                                            key={link.href}
                                            href={link.href}
                                            className="text-sm font-medium transition-all duration-300 hover:opacity-70"
                                            style={{ color: textColor, opacity: 0.75 }}
                                        >
                                            {link.label}
                                        </a>
                                    ))}
                                    <button onClick={onStartStory} className="btn-primary !py-2.5 !px-6 !text-sm">
                                        ابدأ القصة
                                    </button>
                                </nav>

                                {/* Mobile Menu Button */}
                                <button
                                    onClick={() => setMobileMenuOpen(true)}
                                    className="md:hidden p-2 transition-colors"
                                    style={{ color: textColor }}
                                    aria-label="فتح القائمة"
                                >
                                    <Menu size={24} />
                                </button>
                            </div>
                        </div>
                    </header>

                    {/* Mobile Menu Overlay */}
                    <div className={`mobile-menu ${mobileMenuOpen ? 'open' : ''}`}>
                        <button
                            onClick={() => setMobileMenuOpen(false)}
                            className="absolute top-5 right-5 p-2 text-white/70 hover:text-white transition-colors"
                            aria-label="إغلاق القائمة"
                        >
                            <X size={28} />
                        </button>
                        <div className="flex flex-col items-center gap-6">
                            {navLinks.map((link) => (
                                <a
                                    key={link.href}
                                    href={link.href}
                                    onClick={() => setMobileMenuOpen(false)}
                                    className="text-2xl font-medium text-white/80 hover:text-white transition-colors font-display"
                                >
                                    {link.label}
                                </a>
                            ))}
                            <button
                                onClick={() => { setMobileMenuOpen(false); onStartStory(); }}
                                className="btn-primary mt-4"
                            >
                                ابدأ القصة
                            </button>
                        </div>
                    </div>
                </>
            );
        }

        function OpeningScreen({ onBegin }) {
            const [visible, setVisible] = useState(true);
            const [isExiting, setIsExiting] = useState(false);

            const handleBegin = () => {
                setIsExiting(true);
                setTimeout(() => {
                    setVisible(false);
                    onBegin();
                }, 500);
            };

            if (!visible) return null;

            return (
                <div className={`overlay-screen ${isExiting ? 'hidden-overlay' : ''}`}>
                    <Particles count={20} />
                    <div className="relative z-10 text-center px-6">
                        <div className="animate-fadeInUp" style={{ animationDelay: '0.2s' }}>
                            <Sparkles className="mx-auto mb-6 text-gold" size={36} style={{ color: '#d4a853' }} />
                            <h1
                                className="font-display font-bold text-5xl md:text-7xl lg:text-8xl mb-4 tracking-wide"
                                style={{ color: '#f0ede8', textShadow: '0 0 60px rgba(212,168,83,0.2)' }}
                            >
                                {STORY_TITLE}
                            </h1>
                        </div>
                        <div className="animate-fadeInUp" style={{ animationDelay: '0.6s' }}>
                            <p
                                className="font-quote text-xl md:text-2xl lg:text-3xl leading-relaxed mb-10 max-w-2xl mx-auto"
                                style={{ color: 'rgba(240,237,232,0.7)' }}
                            >
                                "{OPENING_QUOTE}"
                            </p>
                        </div>
                        <div className="animate-fadeInUp" style={{ animationDelay: '0.9s' }}>
                            <button onClick={handleBegin} className="btn-primary !text-lg !px-10 !py-4">
                                ابدأ القصة
                                <ArrowLeft size={20} />
                            </button>
                        </div>
                    </div>
                </div>
            );
        }

        function Hero({ onStartJourney, onAbout, currentProgress }) {
            const isLight = currentProgress > 0.5;
            const titleColor = isLight ? '#1a1a2e' : '#f0ede8';
            const textColor = isLight ? 'rgba(26,26,46,0.7)' : 'rgba(240,237,232,0.6)';
            const [inView, setInView] = useState(false);

            useEffect(() => {
                setInView(true);
            }, []);

            return (
                <section id="hero" className="relative min-h-screen flex items-center justify-center overflow-hidden">
                    <Particles count={15} />
                    <div
                        className="absolute inset-0 animate-slowZoom"
                        style={{
                            background: 'radial-gradient(ellipse at 50% 40%, rgba(212,168,83,0.08) 0%, transparent 60%)'
                        }}
                    />
                    <div className="relative z-10 text-center px-6 max-w-4xl mx-auto">
                        <div className={`reveal ${inView ? 'visible' : ''}`}>
                            <p className="font-quote text-lg md:text-xl mb-6" style={{ color: isLight ? '#d4a853' : '#d4a853' }}>
                                <span className="inline-block animate-pulseGlow">✦</span> تجربة قصصية تفاعلية <span className="inline-block animate-pulseGlow">✦</span>
                            </p>
                        </div>
                        <div className={`reveal ${inView ? 'visible' : ''}`} style={{ '--reveal-delay': '150ms' }}>
                            <h1
                                className="font-display font-bold text-4xl md:text-6xl lg:text-7xl leading-snug md:leading-snug mb-6 transition-colors duration-700"
                                style={{ color: titleColor }}
                            >
                                ماذا لو كان أصعب فصل في حياتك…
                                <br />
                                <span style={{ color: '#d4a853' }}>ليس النهاية؟</span>
                            </h1>
                        </div>
                        <div className={`reveal ${inView ? 'visible' : ''}`} style={{ '--reveal-delay': '300ms' }}>
                            <p className="text-lg md:text-2xl leading-relaxed mb-10 max-w-2xl mx-auto transition-colors duration-700" style={{ color: textColor }}>
                                قصة عن الصبر، والأمل، والأيام التي ظننا أننا لن نتجاوزها.
                            </p>
                        </div>
                        <div className={`reveal ${inView ? 'visible' : ''} flex flex-col sm:flex-row items-center justify-center gap-4`} style={{ '--reveal-delay': '450ms' }}>
                            <button onClick={onStartJourney} className="btn-primary !text-lg !px-8 !py-3.5">
                                ابدأ الرحلة
                                <ArrowLeft size={20} />
                            </button>
                            <button onClick={onAbout} className="btn-secondary !text-lg !px-8 !py-3.5">
                                عن القصة
                            </button>
                        </div>
                        <div className={`reveal ${inView ? 'visible' : ''} mt-16`} style={{ '--reveal-delay': '600ms' }}>
                            <ChevronDown className="mx-auto animate-bounce" size={28} style={{ color: isLight ? 'rgba(26,26,46,0.4)' : 'rgba(240,237,232,0.4)' }} />
                        </div>
                    </div>
                    <div className="absolute bottom-0 left-0 right-0 h-40 bg-gradient-to-t from-[#080810] to-transparent" style={{ opacity: isLight ? 0 : 1, transition: 'opacity 0.8s' }} />
                </section>
            );
        }

        function ChapterSection({ chapter, index, progress, onQuestionVisible }) {
            const isLight = progress > 0.7;
            const Icon = chapter.icon;
            const [visible, setVisible] = useState(false);
            const sectionRef = useRef(null);

            useEffect(() => {
                const observer = new IntersectionObserver(
                    (entries) => {
                        entries.forEach((entry) => {
                            if (entry.isIntersecting) setVisible(true);
                        });
                    }, { threshold: 0.2 }
                );
                if (sectionRef.current) observer.observe(sectionRef.current);
                return () => observer.disconnect();
            }, []);

            const titleColor = isLight ? '#1a1a2e' : '#f0ede8';
            const paragraphColor = isLight ? 'rgba(26,26,46,0.75)' : 'rgba(240,237,232,0.7)';

            return (
                <section
                    id={chapter.id}
                    ref={sectionRef}
                    className="chapter-section"
                    style={{ backgroundColor: 'transparent' }}
                >
                    <div className="max-w-3xl mx-auto w-full">
                        <div className={`reveal ${visible ? 'visible' : ''} text-center mb-8`}>
                            <Icon
                                className="mx-auto mb-4"
                                size={32}
                                style={{ color: isLight ? '#d4a853' : '#d4a853', opacity: 0.8 }}
                            />
                            <h2
                                className="font-display font-bold text-3xl md:text-4xl lg:text-5xl mb-2 transition-colors duration-700"
                                style={{ color: titleColor }}
                            >
                                {chapter.title}
                            </h2>
                            <div
                                className="w-12 h-0.5 mx-auto mt-4"
                                style={{ backgroundColor: isLight ? 'rgba(212,168,83,0.5)' : 'rgba(212,168,83,0.4)' }}
                            />
                        </div>
                        <div className="space-y-5 md:space-y-6">
                            {chapter.paragraphs.map((para, pIndex) => (
                                <p
                                    key={pIndex}
                                    className={`reveal ${visible ? 'visible' : ''} font-body text-base md:text-lg lg:text-xl leading-loose md:leading-loose transition-colors duration-700`}
                                    style={{
                                        '--reveal-delay': `${pIndex * 180}ms`,
                                        color: paragraphColor,
                                        textAlign: 'center',
                                        maxWidth: '600px',
                                        marginLeft: 'auto',
                                        marginRight: 'auto'
                                    }}
                                >
                                    {para}
                                </p>
                            ))}
                        </div>
                    </div>
                </section>
            );
        }

        function QuoteBlock({ text, progress, visible }) {
            const isLight = progress > 0.7;
            return (
                <div className="quote-block relative">
                    <div className={`reveal-fade-only ${visible ? 'visible' : ''}`}>
                        <div
                            className="text-5xl md:text-6xl mb-4 font-quote"
                            style={{ color: isLight ? 'rgba(212,168,83,0.5)' : 'rgba(212,168,83,0.35)', lineHeight: 1 }}
                        >
                            "
                        </div>
                        <p
                            className="font-quote text-xl md:text-2xl lg:text-3xl leading-relaxed transition-colors duration-700"
                            style={{ color: isLight ? '#1a1a2e' : '#f0ede8', opacity: 0.85 }}
                        >
                            {text}
                        </p>
                        <div
                            className="text-5xl md:text-6xl mt-2 font-quote"
                            style={{ color: isLight ? 'rgba(212,168,83,0.5)' : 'rgba(212,168,83,0.35)', lineHeight: 1 }}
                        >
                            "
                        </div>
                    </div>
                </div>
            );
        }

        function InteractiveQuestion({ question, progress, isLight }) {
            const [answer, setAnswer] = useLocalStorage(question.storageKey);
            const [saved, setSaved] = useState(!!answer);
            const [showSaved, setShowSaved] = useState(false);

            const handleSave = () => {
                if (answer.trim()) {
                    setSaved(true);
                    setShowSaved(true);
                    setTimeout(() => setShowSaved(false), 3000);
                }
            };

            return (
                <div className="max-w-xl mx-auto px-6 py-8 text-center">
                    <div className="reveal-fade-only visible">
                        <MessageCircle className="mx-auto mb-4" size={28} style={{ color: isLight ? '#d4a853' : '#d4a853', opacity: 0.7 }} />
                        <p
                            className="font-display text-xl md:text-2xl mb-5 transition-colors duration-700"
                            style={{ color: isLight ? '#1a1a2e' : '#f0ede8', opacity: 0.85 }}
                        >
                            {question.label}
                        </p>
                        <textarea
                            value={answer}
                            onChange={(e) => setAnswer(e.target.value)}
                            className="story-input"
                            placeholder={question.placeholder}
                            style={{ color: isLight ? '#1a1a2e' : '#f0ede8', backgroundColor: isLight ? 'rgba(255,255,255,0.4)' : 'rgba(255,255,255,0.05)', borderColor: isLight ? 'rgba(26,26,46,0.2)' : 'rgba(255,255,255,0.15)' }}
                        />
                        <div className="mt-4 flex items-center justify-center gap-3 flex-wrap">
                            <button onClick={handleSave} className="btn-primary !py-2.5 !px-6 !text-sm">
                                {saved ? 'تم الحفظ' : 'احفظ الإجابة'}
                                {saved && <CheckCircle2 size={16} />}
                            </button>
                            {saved && !showSaved && (
                                <span className="text-sm" style={{ color: isLight ? 'rgba(26,26,46,0.5)' : 'rgba(240,237,232,0.5)' }}>
                                    محفوظة في متصفحك فقط
                                </span>
                            )}
                        </div>
                    </div>
                </div>
            );
        }

        function FinalMessageSection({ progress, isLight }) {
            const [message, setMessage] = useLocalStorage(finalMessagePrompt.storageKey);
            const [copied, setCopied] = useState(false);

            const handleCopy = () => {
                if (message) {
                    navigator.clipboard?.writeText(message).then(() => {
                        setCopied(true);
                        setTimeout(() => setCopied(false), 2500);
                    }).catch(() => {});
                }
            };

            const handleDownload = () => {
                if (!message) return;
                const blob = new Blob([message], { type: 'text/plain;charset=utf-8' });
                const url = URL.createObjectURL(blob);
                const a = document.createElement('a');
                a.href = url;
                a.download = `رسالة-لنفسي-${new Date().toISOString().slice(0,10)}.txt`;
                a.click();
                URL.revokeObjectURL(url);
            };

            return (
                <div className="max-w-xl mx-auto px-6 py-8 text-center">
                    <Feather className="mx-auto mb-4" size={28} style={{ color: isLight ? '#d4a853' : '#d4a853', opacity: 0.7 }} />
                    <p
                        className="font-display text-xl md:text-2xl mb-5 transition-colors duration-700"
                        style={{ color: isLight ? '#1a1a2e' : '#f0ede8', opacity: 0.85 }}
                    >
                        {finalMessagePrompt.label}
                    </p>
                    <textarea
                        value={message}
                        onChange={(e) => setMessage(e.target.value)}
                        className="story-input"
                        placeholder={finalMessagePrompt.placeholder}
                        style={{ color: isLight ? '#1a1a2e' : '#f0ede8', backgroundColor: isLight ? 'rgba(255,255,255,0.4)' : 'rgba(255,255,255,0.05)', borderColor: isLight ? 'rgba(26,26,46,0.2)' : 'rgba(255,255,255,0.15)' }}
                    />
                    <div className="mt-4 flex items-center justify-center gap-3 flex-wrap">
                        <button onClick={handleCopy} className="btn-secondary !py-2.5 !px-6 !text-sm" style={{ borderColor: isLight ? 'rgba(26,26,46,0.3)' : 'rgba(255,255,255,0.2)', color: isLight ? '#1a1a2e' : '#f0ede8' }}>
                            {copied ? 'تم النسخ ✓' : 'احتفظ بهذه الرسالة'}
                            <Copy size={16} />
                        </button>
                        <button onClick={handleDownload} className="btn-secondary !py-2.5 !px-6 !text-sm" style={{ borderColor: isLight ? 'rgba(26,26,46,0.3)' : 'rgba(255,255,255,0.2)', color: isLight ? '#1a1a2e' : '#f0ede8' }}>
                            تحميل الرسالة
                            <Download size={16} />
                        </button>
                    </div>
                    <p className="mt-4 text-xs" style={{ color: isLight ? 'rgba(26,26,46,0.4)' : 'rgba(240,237,232,0.4)' }}>
                        تُحفظ رسالتك محليًا في متصفحك فقط. لا تُرسل لأي شخص ولا تُعرض للعامة.
                    </p>
                </div>
            );
        }

        function ClosingScreen({ onRestart, isVisible }) {
            const [step, setStep] = useState(0);

            useEffect(() => {
                if (isVisible) {
                    setStep(0);
                    const timer1 = setTimeout(() => setStep(1), 1500);
                    const timer2 = setTimeout(() => setStep(2), 2800);
                    const timer3 = setTimeout(() => setStep(3), 3800);
                    return () => { clearTimeout(timer1); clearTimeout(timer2); clearTimeout(timer3); };
                }
            }, [isVisible]);

            if (!isVisible) return null;

            return (
                <div className="overlay-screen" style={{ zIndex: 1100, background: '#f5f0e8' }}>
                    <Particles count={12} />
                    <div className="relative z-10 text-center px-6 max-w-2xl">
                        {step >= 0 && (
                            <div className="animate-fadeInUp" style={{ color: '#1a1a2e' }}>
                                <p className="font-quote text-2xl md:text-3xl mb-6" style={{ color: 'rgba(26,26,46,0.6)' }}>
                                    وهنا تنتهي القصة…
                                </p>
                            </div>
                        )}
                        {step >= 1 && (
                            <div className="animate-fadeInUp" style={{ animationDelay: '0.3s', color: '#1a1a2e' }}>
                                <p className="font-quote text-2xl md:text-3xl mb-6" style={{ color: 'rgba(26,26,46,0.7)' }}>
                                    …لكن قصتك أنت ما زالت مستمرة.
                                </p>
                            </div>
                        )}
                        {step >= 2 && (
                            <div className="animate-fadeInUp" style={{ animationDelay: '0.6s' }}>
                                <h2 className="font-display font-bold text-4xl md:text-6xl mb-4" style={{ color: '#1a1a2e' }}>
                                    {STORY_TITLE}
                                </h2>
                            </div>
                        )}
                        {step >= 2 && (
                            <div className="animate-fadeInUp" style={{ animationDelay: '0.9s' }}>
                                <p className="font-quote text-3xl md:text-4xl mb-8" style={{ color: '#d4a853' }}>
                                    استمر.
                                </p>
                            </div>
                        )}
                        {step >= 3 && (
                            <div className="animate-fadeInUp" style={{ animationDelay: '1.1s' }}>
                                <button onClick={onRestart} className="btn-primary !text-lg !px-8 !py-3.5">
                                    <RotateCcw size={18} />
                                    ابدأ من جديد
                                </button>
                            </div>
                        )}
                    </div>
                </div>
            );
        }

        function AboutPage({ progress }) {
            const isLight = progress > 0.5;
            const [visible, setVisible] = useState(false);
            const aboutRef = useRef(null);

            useEffect(() => {
                const observer = new IntersectionObserver(
                    (entries) => {
                        entries.forEach((entry) => {
                            if (entry.isIntersecting) setVisible(true);
                        });
                    }, { threshold: 0.2 }
                );
                if (aboutRef.current) observer.observe(aboutRef.current);
                return () => observer.disconnect();
            }, []);

            const titleColor = isLight ? '#1a1a2e' : '#f0ede8';
            const textColor = isLight ? 'rgba(26,26,46,0.7)' : 'rgba(240,237,232,0.65)';

            const topics = [
                { icon: Heart, label: 'الأمل' },
                { icon: CloudSun, label: 'الصبر' },
                { icon: Wind, label: 'الاستمرار' },
                { icon: Sparkles, label: 'تجاوز الفترات الصعبة' },
                { icon: Sun, label: 'الإيمان بالتغيير' }
            ];

            return (
                <section id="about" ref={aboutRef} className="py-20 md:py-28 px-6">
                    <div className="max-w-3xl mx-auto text-center">
                        <div className={`reveal ${visible ? 'visible' : ''}`}>
                            <h2 className="font-display font-bold text-3xl md:text-4xl lg:text-5xl mb-6 transition-colors duration-700" style={{ color: titleColor }}>
                                عن {STORY_TITLE}
                            </h2>
                        </div>
                        <div className={`reveal ${visible ? 'visible' : ''}`} style={{ '--reveal-delay': '150ms' }}>
                            <p className="text-base md:text-lg leading-loose mb-8 transition-colors duration-700" style={{ color: textColor }}>
                                "{STORY_TITLE}" ليست مجرد موقع. إنها تجربة قصصية تفاعلية صُممت لتشعرك أنك لست وحدك.
                                إنها رحلة إنسانية تنطلق من أعماق التجربة الصعبة لتصل إلى نور الأمل.
                            </p>
                            <p className="text-base md:text-lg leading-loose mb-10 transition-colors duration-700" style={{ color: textColor }}>
                                هذا المشروع ليس وعظًا ولا درسًا. إنه مرآة صادقة للرحلة التي يمر بها كثير منا —
                                من الحيرة والثقل، إلى الصبر، ثم إلى النور الذي يبدأ صغيرًا ويكبر.
                            </p>
                        </div>
                        <div className={`reveal ${visible ? 'visible' : ''} flex flex-wrap items-center justify-center gap-3 md:gap-4`} style={{ '--reveal-delay': '300ms' }}>
                            {topics.map((topic) => {
                                const TopicIcon = topic.icon;
                                return (
                                    <span
                                        key={topic.label}
                                        className="inline-flex items-center gap-2 px-4 py-2 rounded-full text-sm font-medium transition-colors duration-500"
                                        style={{
                                            backgroundColor: isLight ? 'rgba(26,26,46,0.06)' : 'rgba(255,255,255,0.06)',
                                            color: isLight ? '#1a1a2e' : '#f0ede8',
                                            border: `1px solid ${isLight ? 'rgba(26,26,46,0.1)' : 'rgba(255,255,255,0.1)'}`
                                        }}
                                    >
                                        <TopicIcon size={16} style={{ color: '#d4a853' }} />
                                        {topic.label}
                                    </span>
                                );
                            })}
                        </div>
                    </div>
                </section>
            );
        }

        function Footer({ progress }) {
            const isLight = progress > 0.65;
            const textColor = isLight ? '#1a1a2e' : '#f0ede8';
            const mutedColor = isLight ? 'rgba(26,26,46,0.5)' : 'rgba(240,237,232,0.5)';

            return (
                <footer
                    className="py-12 px-6 border-t transition-colors duration-700"
                    style={{
                        borderColor: isLight ? 'rgba(26,26,46,0.1)' : 'rgba(255,255,255,0.08)',
                        backgroundColor: 'transparent'
                    }}
                >
                    <div className="max-w-6xl mx-auto">
                        <div className="flex flex-col md:flex-row items-center justify-between gap-6 mb-8">
                            <div className="text-center md:text-right">
                                <h3 className="font-display font-bold text-2xl mb-2" style={{ color: textColor }}>
                                    {STORY_TITLE}
                                </h3>
                                <p className="text-sm" style={{ color: mutedColor }}>
                                    قصة عن الأمل والصبر والاستمرار.
                                </p>
                            </div>
                            <div className="flex items-center gap-6 flex-wrap justify-center">
                                <a href="#story" className="text-sm transition-opacity hover:opacity-70" style={{ color: mutedColor }}>القصة</a>
                                <a href="#about" className="text-sm transition-opacity hover:opacity-70" style={{ color: mutedColor }}>عن المشروع</a>
                                <a href="#privacy" className="text-sm transition-opacity hover:opacity-70 flex items-center gap-1" style={{ color: mutedColor }}>
                                    <Shield size={14} /> الخصوصية
                                </a>
                                <a href="#contact" className="text-sm transition-opacity hover:opacity-70 flex items-center gap-1" style={{ color: mutedColor }}>
                                    <Mail size={14} /> تواصل معنا
                                </a>
                            </div>
                        </div>
                        <div className="text-center pt-6 border-t" style={{ borderColor: isLight ? 'rgba(26,26,46,0.08)' : 'rgba(255,255,255,0.06)' }}>
                            <p className="text-xs" style={{ color: mutedColor }}>
                                © 2026 {STORY_TITLE} — جميع الحقوق محفوظة
                            </p>
                        </div>
                    </div>
                </footer>
            );
        }

        function MusicToggle({ isLight }) {
            const [playing, setPlaying] = useState(false);
            const audioRef = useRef(null);

            const toggleMusic = () => {
                if (playing) {
                    audioRef.current?.pause();
                    setPlaying(false);
                } else {
                    // Note: Replace with an actual royalty-free audio file URL
                    if (audioRef.current) {
                        audioRef.current.volume = 0.3;
                        audioRef.current.play().catch(() => {});
                        setPlaying(true);
                    } else {
                        // Create a simple ambient tone using Web Audio API
                        try {
                            const AudioContext = window.AudioContext || window.webkitAudioContext;
                            const ctx = new AudioContext();
                            const oscillator = ctx.createOscillator();
                            const gain = ctx.createGain();
                            oscillator.connect(gain);
                            gain.connect(ctx.destination);
                            oscillator.frequency.value = 174; // low ambient frequency
                            oscillator.type = 'sine';
                            gain.gain.value = 0.05;
                            gain.gain.exponentialRampToValueAtTime(0.02, ctx.currentTime + 2);
                            oscillator.start();
                            audioRef.current = { pause: () => { oscillator.stop(); ctx.close(); }, play: () => {} };
                            setPlaying(true);
                            audioRef.current.pause = () => { oscillator.stop(); ctx.close(); };
                        } catch {
                            // Audio not supported
                        }
                    }
                }
            };

            return (
                <>
                    <button
                        onClick={toggleMusic}
                        className="fixed bottom-6 left-6 z-40 p-3 rounded-full transition-all duration-400 shadow-lg"
                        style={{
                            backgroundColor: isLight ? 'rgba(26,26,46,0.08)' : 'rgba(255,255,255,0.06)',
                            color: isLight ? '#1a1a2e' : '#f0ede8',
                            border: `1px solid ${isLight ? 'rgba(26,26,46,0.1)' : 'rgba(255,255,255,0.1)'}`,
                            backdropFilter: 'blur(8px)'
                        }}
                        aria-label={playing ? 'إيقاف الموسيقى' : 'تشغيل الموسيقى'}
                        title={playing ? 'إيقاف الموسيقى' : 'تشغيل الموسيقى'}
                    >
                        {playing ? <Pause size={20} /> : <Music size={20} />}
                    </button>
                </>
            );
        }

        function App() {
            const [showOpening, setShowOpening] = useState(true);
            const [showClosing, setShowClosing] = useState(false);
            const storyRef = useRef(null);
            const { progress } = useScrollProgress(storyRef);
            const bgColor = getBackgroundColor(progress);
            const textColor = getTextColor(progress);
            const isLight = progress > 0.7;

            // Update body background color
            useEffect(() => {
                document.body.style.backgroundColor = bgColor;
            }, [bgColor]);

            // Apply scroll reveal
            useEffect(() => {
                const observer = new IntersectionObserver(
                    (entries) => {
                        entries.forEach((entry) => {
                            if (entry.isIntersecting) {
                                entry.target.classList.add('visible');
                            }
                        });
                    },
                    { threshold: 0.1, rootMargin: '0px 0px -30px 0px' }
                );
                const elements = document.querySelectorAll('.reveal, .reveal-fade-only');
                elements.forEach((el) => observer.observe(el));
                return () => elements.forEach((el) => observer.unobserve(el));
            }, []);

            const handleBeginStory = () => {
                setShowOpening(false);
                setTimeout(() => {
                    document.getElementById('story')?.scrollIntoView({ behavior: 'smooth' });
                }, 100);
            };

            const handleStartJourney = () => {
                document.getElementById('story')?.scrollIntoView({ behavior: 'smooth' });
            };

            const handleAboutClick = () => {
                document.getElementById('about')?.scrollIntoView({ behavior: 'smooth' });
            };

            const handleRestart = () => {
                setShowClosing(false);
                setTimeout(() => {
                    window.scrollTo({ top: 0, behavior: 'smooth' });
                    setTimeout(() => {
                        document.getElementById('story')?.scrollIntoView({ behavior: 'smooth' });
                    }, 300);
                }, 100);
            };

            const handleReRead = () => {
                document.getElementById('story')?.scrollIntoView({ behavior: 'smooth' });
            };

            // Auto-show closing screen when at end
            useEffect(() => {
                if (progress > 0.92 && !showOpening) {
                    const timer = setTimeout(() => setShowClosing(true), 1200);
                    return () => clearTimeout(timer);
                }
            }, [progress, showOpening]);

            return (
                <>
                    {showOpening && <OpeningScreen onBegin={handleBeginStory} />}
                    <ClosingScreen onRestart={handleRestart} isVisible={showClosing} />

                    <Navbar onStartStory={handleStartJourney} currentProgress={progress} />

                    {/* Fixed Background Layer */}
                    <div
                        className="bg-layer"
                        style={{ backgroundColor: bgColor }}
                    />

                    <main className="content-layer">
                        <Hero onStartJourney={handleStartJourney} onAbout={handleAboutClick} currentProgress={progress} />

                        {/* Chapters Overview */}
                        <div id="chapters-overview" className="py-10 px-6 text-center">
                            <div className="max-w-4xl mx-auto">
                                <p className="font-quote text-lg md:text-xl mb-6" style={{ color: isLight ? 'rgba(26,26,46,0.5)' : 'rgba(240,237,232,0.5)' }}>
                                    رحلة من ستة فصول
                                </p>
                                <div className="flex flex-wrap justify-center gap-3">
                                    {storyChapters.map((ch, i) => {
                                        const Icon = ch.icon;
                                        return (
                                            <a
                                                key={ch.id}
                                                href={`#${ch.id}`}
                                                className="inline-flex items-center gap-2 px-4 py-2 rounded-full text-sm transition-all duration-300 hover:scale-105"
                                                style={{
                                                    backgroundColor: isLight ? 'rgba(26,26,46,0.06)' : 'rgba(255,255,255,0.04)',
                                                    color: isLight ? '#1a1a2e' : '#f0ede8',
                                                    border: `1px solid ${isLight ? 'rgba(26,26,46,0.1)' : 'rgba(255,255,255,0.08)'}`
                                                }}
                                            >
                                                <Icon size={14} style={{ color: '#d4a853' }} />
                                                {i + 1}. {ch.title.replace(/^الفصل\s+\S+\s*—\s*/, '')}
                                            </a>
                                        );
                                    })}
                                </div>
                            </div>
                        </div>

                        {/* Story Section */}
                        <div id="story" ref={storyRef} className="story-scroll-container">
                            {/* Chapter 1 */}
                            <ChapterSection
                                chapter={storyChapters[0]}
                                index={0}
                                progress={progress}
                                onQuestionVisible={() => {}}
                            />

                            {/* Quote after Chapter 1 */}
                            <QuoteBlock text={quotes[0]} progress={progress} visible={progress > 0.05} />

                            {/* Chapter 2 */}
                            <ChapterSection
                                chapter={storyChapters[1]}
                                index={1}
                                progress={progress}
                                onQuestionVisible={() => {}}
                            />

                            {/* Interactive Question 1 */}
                            <InteractiveQuestion question={interactiveQuestions[0]} progress={progress} isLight={isLight} />

                            {/* Quote after Chapter 2 */}
                            <QuoteBlock text={quotes[1]} progress={progress} visible={progress > 0.25} />

                            {/* Chapter 3 */}
                            <ChapterSection
                                chapter={storyChapters[2]}
                                index={2}
                                progress={progress}
                                onQuestionVisible={() => {}}
                            />

                            {/* Chapter 4 */}
                            <ChapterSection
                                chapter={storyChapters[3]}
                                index={3}
                                progress={progress}
                                onQuestionVisible={() => {}}
                            />

                            {/* Quote after Chapter 4 */}
                            <QuoteBlock text={quotes[2]} progress={progress} visible={progress > 0.55} />

                            {/* Chapter 5 */}
                            <ChapterSection
                                chapter={storyChapters[4]}
                                index={4}
                                progress={progress}
                                onQuestionVisible={() => {}}
                            />

                            {/* Interactive Question 2 */}
                            <InteractiveQuestion question={interactiveQuestions[1]} progress={progress} isLight={isLight} />

                            {/* Chapter 6 */}
                            <ChapterSection
                                chapter={storyChapters[5]}
                                index={5}
                                progress={progress}
                                onQuestionVisible={() => {}}
                            />

                            {/* Final Message */}
                            <FinalMessageSection progress={progress} isLight={isLight} />

                            {/* Post-story buttons */}
                            <div className="py-12 px-6 text-center">
                                <div className="flex flex-col sm:flex-row items-center justify-center gap-4">
                                    <button onClick={handleReRead} className="btn-primary !py-3 !px-7">
                                        <RotateCcw size={18} />
                                        أعد قراءة القصة
                                    </button>
                                    <button onClick={handleRestart} className="btn-secondary !py-3 !px-7" style={{ borderColor: isLight ? 'rgba(26,26,46,0.25)' : 'rgba(255,255,255,0.2)', color: isLight ? '#1a1a2e' : '#f0ede8' }}>
                                        <Sparkles size={18} />
                                        ابدأ من جديد
                                    </button>
                                </div>
                            </div>
                        </div>

                        {/* About Section */}
                        <AboutPage progress={progress} />

                        {/* Privacy & Contact placeholder sections */}
                        <div id="privacy" className="py-16 px-6 text-center max-w-2xl mx-auto">
                            <h3 className="font-display font-bold text-2xl mb-4 transition-colors duration-700" style={{ color: isLight ? '#1a1a2e' : '#f0ede8' }}>
                                الخصوصية
                            </h3>
                            <p className="text-sm leading-relaxed transition-colors duration-700" style={{ color: isLight ? 'rgba(26,26,46,0.6)' : 'rgba(240,237,232,0.6)' }}>
                                جميع الرسائل والإجابات التي تكتبها تُحفظ محليًا في متصفحك فقط.
                                لا تُرسل إلى أي خادم، ولا تُشارك مع أي طرف ثالث، ولا تُعرض للعامة.
                                بياناتك تبقى ملكك وحدك.
                            </p>
                        </div>
                        <div id="contact" className="py-16 px-6 text-center max-w-2xl mx-auto">
                            <h3 className="font-display font-bold text-2xl mb-4 transition-colors duration-700" style={{ color: isLight ? '#1a1a2e' : '#f0ede8' }}>
                                تواصل معنا
                            </h3>
                            <p className="text-sm leading-relaxed transition-colors duration-700" style={{ color: isLight ? 'rgba(26,26,46,0.6)' : 'rgba(240,237,232,0.6)' }}>
                                إذا أردت مشاركة تجربتك أو لديك اقتراح، يسعدنا أن نسمع منك.
                                هذا المشروع صُنع بحب لكل من يمر برحلة صعبة.
                            </p>
                        </div>

                        <Footer progress={progress} />
                    </main>

                    <MusicToggle isLight={isLight} />
                </>
            );
        }

        // ===== RENDER =====
        const root = createRoot(document.getElementById('root'));
        root.render(<App />);
    </script>
</body>
</html>