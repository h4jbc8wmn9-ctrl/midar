<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>البوابة الشاملة لمشروع مدار | MIDAR Space & Biometric Fintech</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Tajawal & Orbitron -->
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600;800;900&family=Tajawal:wght@300;400;500;700;800;900&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        space: {
                            950: '#02040A',
                            900: '#060B18',
                            800: '#0D1B36',
                            700: '#162C54',
                        },
                        cyan: {
                            glow: '#00F0FF',
                            neon: '#00D8F6'
                        }
                    },
                    fontFamily: {
                        tajawal: ['Tajawal', 'sans-serif'],
                        orbitron: ['Orbitron', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Tajawal', sans-serif;
            background-color: #02040A;
            color: #E2E8F0;
            overflow-x: hidden;
        }

    /* Ambient Lighting */
    .ambient-glow-cyan {
        position: fixed;
        width: 600px;
        height: 600px;
        border-radius: 50%;
        background: radial-gradient(circle, rgba(0, 240, 255, 0.08) 0%, rgba(2, 4, 10, 0) 70%);
        top: -200px;
        right: -200px;
        pointer-events: none;
        z-index: 0;
    }

    .ambient-glow-blue {
        position: fixed;
        width: 700px;
        height: 700px;
        border-radius: 50%;
        background: radial-gradient(circle, rgba(22, 44, 84, 0.35) 0%, rgba(2, 4, 10, 0) 70%);
        bottom: -250px;
        left: -250px;
        pointer-events: none;
        z-index: 0;
    }

    /* Glassmorphism Styles */
    .glass-panel {
        background: rgba(13, 27, 54, 0.5);
        backdrop-filter: blur(16px);
        -webkit-backdrop-filter: blur(16px);
        border: 1px solid rgba(0, 240, 255, 0.18);
        box-shadow: 0 10px 40px -10px rgba(0, 0, 0, 0.6);
    }

    .glass-panel-hover:hover {
        border-color: rgba(0, 240, 255, 0.5);
        box-shadow: 0 0 25px rgba(0, 240, 255, 0.2);
        transform: translateY(-2px);
    }

    /* Sci-Fi Circuit Borders & Glows */
    .glow-text {
        text-shadow: 0 0 10px rgba(0, 240, 255, 0.6);
    }

    /* Custom Scrollbar */
    ::-webkit-scrollbar {
        width: 6px;
        height: 6px;
    }
    ::-webkit-scrollbar-track {
        background: #060B18;
    }
    ::-webkit-scrollbar-thumb {
        background: #162C54;
        border-radius: 3px;
        border: 1px solid rgba(0, 240, 255, 0.3);
    }
    ::-webkit-scrollbar-thumb:hover {
        background: #00F0FF;
    }

    .star-rating i {
        cursor: pointer;
        transition: color 0.2s ease, transform 0.2s ease;
    }
    .star-rating i:hover {
        transform: scale(1.25);
    }

    /* Animated Grid Overlay */
    .grid-pattern {
        background-size: 40px 40px;
        background-image: 
            linear-gradient(to right, rgba(0, 240, 255, 0.03) 1px, transparent 1px),
            linear-gradient(to bottom, rgba(0, 240, 255, 0.03) 1px, transparent 1px);
    }
</style>
</head>
<body class="min-h-screen flex flex-col justify-between relative grid-pattern selection:bg-cyan-500 selection:text-black">

<!-- Ambient Lighting Effects -->
<div class="ambient-glow-cyan"></div>
<div class="ambient-glow-blue"></div>

<!-- NAVIGATION HEADER -->
<header class="sticky top-0 z-40 w-full glass-panel border-b border-cyan-500/20 bg-space-950/80">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
        <!-- Brand Info -->
        <div class="flex items-center space-x-3 space-x-reverse cursor-pointer" onclick="switchTab('all')">
            <div class="relative w-12 h-12 flex items-center justify-center">
                <div class="absolute inset-0 bg-cyan-glow/20 rounded-full blur-md"></div>
                <svg viewBox="0 0 200 200" class="w-full h-full relative z-10 drop-shadow-[0_0_10px_rgba(0,240,255,0.8)]">
                    <ellipse cx="100" cy="100" rx="85" ry="32" fill="none" stroke="#00F0FF" stroke-width="8" transform="rotate(-25 100 100)"/>
                    <circle cx="165" cy="65" r="9" fill="#00F0FF" />
                    <path d="M 55,145 L 55,65 L 100,115 L 145,65 L 145,145" fill="none" stroke="#38BDF8" stroke-width="16" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </div>
            <div>
                <h1 class="text-xl font-extrabold text-white tracking-wide font-orbitron">M I D A R</h1>
                <p class="text-xs text-cyan-glow font-bold tracking-widest">منظومة الفضاء والخدمات الحيوية</p>
            </div>
        </div>

        <!-- Quick Action Links -->
        <div class="flex items-center space-x-3 space-x-reverse">
            <button onclick="openModal('https://docs.google.com/forms/d/e/1FAIpQLSdgG47sWzhxxwDQ6fVb0FGin_vFktz4S9xz7PuIRPekMPoN-Q/viewform?usp=header')" class="px-4 py-2 rounded-xl bg-cyan-500/10 border border-cyan-500/40 text-cyan-glow hover:bg-cyan-500 hover:text-black font-bold text-xs sm:text-sm transition-all flex items-center gap-2 shadow-[0_0_15px_rgba(0,240,255,0.15)]">
                <i class="fa-solid fa-star-half-stroke"></i>
                <span>تقييم تجربة العرض</span>
            </button>
        </div>
    </div>
</header>

<!-- HERO SECTION -->
<section class="relative z-10 max-w-7xl mx-auto px-4 pt-8 pb-4 text-center">
    <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-cyan-950/60 border border-cyan-500/30 text-cyan-400 text-xs font-semibold mb-4">
        <span class="w-2 h-2 rounded-full bg-cyan-400 animate-ping"></span>
        معرض مشروع مدار 2026 - التوثيق الهيكلي الشامل
    </div>
    <h2 class="text-3xl sm:text-5xl font-black text-white leading-tight mb-3">
        كل أموالك في <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-glow to-blue-500 glow-text">مَـــدَار أذكى</span>
    </h2>
    <p class="text-gray-400 text-sm sm:text-base max-w-3xl mx-auto leading-relaxed">
        استكشف الرسوم الهيكلية الستة المبتكرة لشبكة الخدمات المالية الحيوية، ابتداءً من الأجهزة القابلة للارتداء والتحليل البيومتري، وحتى الاقتصاد المجتمعي والكاش الكريستالي.
    </p>

    <!-- FILTER TABS NAV -->
    <div class="flex items-center justify-center gap-2 sm:gap-3 flex-wrap mt-8">
        <button onclick="filterComponents('all')" id="tab-all" class="tab-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-bold bg-cyan-500 text-black shadow-[0_0_15px_rgba(0,240,255,0.4)] transition-all">
            جميع الأنظمة (6)
        </button>
        <button onclick="filterComponents('wearables')" id="tab-wearables" class="tab-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-bold bg-space-800 text-gray-300 border border-cyan-500/20 hover:border-cyan-500/50 transition-all">
            1. الأجهزة والتحقق
        </button>
        <button onclick="filterComponents('capsule')" id="tab-capsule" class="tab-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-bold bg-space-800 text-gray-300 border border-cyan-500/20 hover:border-cyan-500/50 transition-all">
            2. كبسولة التحليل
        </button>
        <button onclick="filterComponents('wristband')" id="tab-wristband" class="tab-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-bold bg-space-800 text-gray-300 border border-cyan-500/20 hover:border-cyan-500/50 transition-all">
            3. سوار الهولوجرام
        </button>
        <button onclick="filterComponents('vaults')" id="tab-vaults" class="tab-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-bold bg-space-800 text-gray-300 border border-cyan-500/20 hover:border-cyan-500/50 transition-all">
            4. العقود الذكية
        </button>
        <button onclick="filterComponents('kitchen')" id="tab-kitchen" class="tab-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-bold bg-space-800 text-gray-300 border border-cyan-500/20 hover:border-cyan-500/50 transition-all">
            5. المطبخ الذكي
        </button>
        <button onclick="filterComponents('crystal')" id="tab-crystal" class="tab-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-bold bg-space-800 text-gray-300 border border-cyan-500/20 hover:border-cyan-500/50 transition-all">
            6. الكاش الكريستالي
        </button>
    </div>
</section>

<!-- CORE 6 DIAGRAMS GRID DISPLAY -->
<main class="relative z-10 max-w-7xl mx-auto px-4 py-8 w-full">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6" id="diagramsContainer">

        <!-- DIAGRAM 1: WEARABLES & BIOMETRICS -->
        <div class="diagram-card glass-panel glass-panel-hover rounded-2xl p-6 flex flex-col justify-between transition-all duration-300" data-category="wearables">
            <div>
                <div class="flex items-center justify-between mb-4">
                    <span class="text-xs font-mono font-bold text-cyan-glow bg-cyan-950/80 px-3 py-1 rounded-full border border-cyan-500/30">رسم (1)</span>
                    <div class="w-10 h-10 rounded-xl bg-cyan-500/10 text-cyan-glow flex items-center justify-center text-lg">
                        <i class="fa-solid fa-glasses"></i>
                    </div>
                </div>
                <h3 class="text-xl font-bold text-white mb-2">الأجهزة القابلة للارتداء وسائط التحقق</h3>
                <p class="text-xs text-gray-400 leading-relaxed mb-4">أنظمة إلغاء البطاقات والصرافات واستبدالها بالتحقق البيولوجي المباشر والتوقيع المشفر.</p>

                <!-- Core Sub-points List -->
                <ul class="space-y-2 text-xs text-gray-300">
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-microchip text-cyan-400"></i>
                        <span><strong>1a:</strong> شريحة إلكترونية تحت الجلد (إلغاء الصرافات).</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-[#00F0FF] fa-fingerprint text-cyan-400"></i>
                        <span><strong>1b:</strong> وسائط التحقق ولهوية البيولوجية المدمجة.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-walk text-cyan-400"></i>
                        <span><strong>1c:</strong> التعرف الحركي والصوتي (نبرة صوت وبنية مشية).</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-vr-cardboard text-cyan-400"></i>
                        <span><strong>1d:</strong> نظارات XR والعدسات + التوقيع المشفر في الهواء.</span>
                    </li>
                </ul>
            </div>
            <button onclick="openDetailModal('modal-1')" class="mt-6 w-full py-2.5 bg-cyan-500/10 hover:bg-cyan-500 hover:text-slate-950 text-cyan-glow font-bold text-xs rounded-xl border border-cyan-500/30 transition-all flex items-center justify-center gap-2">
                <span>عرض التفاصيل الكاملة</span>
                <i class="fa-solid fa-arrow-left"></i>
            </button>
        </div>

        <!-- DIAGRAM 2: BIOMETRIC CAPSULE -->
        <div class="diagram-card glass-panel glass-panel-hover rounded-2xl p-6 flex flex-col justify-between transition-all duration-300" data-category="capsule">
            <div>
                <div class="flex items-center justify-between mb-4">
                    <span class="text-xs font-mono font-bold text-cyan-glow bg-cyan-950/80 px-3 py-1 rounded-full border border-cyan-500/30">رسم (2)</span>
                    <div class="w-10 h-10 rounded-xl bg-cyan-500/10 text-cyan-glow flex items-center justify-center text-lg">
                        <i class="fa-solid fa-capsules"></i>
                    </div>
                </div>
                <h3 class="text-xl font-bold text-white mb-2">كبسولة التحليل البيومتري والبنك التنبؤي</h3>
                <p class="text-xs text-gray-400 leading-relaxed mb-4">كبسولة معزولة توفر مستشار المشاعر اللحظية والتوأم المالي الرقمي مع أمان فوري.</p>

                <ul class="space-y-2 text-xs text-gray-300">
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-heart-pulse text-cyan-400"></i>
                        <span><strong>2a:</strong> مصادقة المشاعر ونبض القلب البيومتري.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-shield-halved text-cyan-400"></i>
                        <span><strong>2b:</strong> وقف العمليات مؤقتاً عند عدم الاتزان النفسي.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-diagram-project text-cyan-400"></i>
                        <span><strong>2c:</strong> التوأم المالي الرقمي محاكاة نتائج القرارات.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-bolt text-cyan-400"></i>
                        <span><strong>2d:</strong> زمن انتظار صفر (حلول الذكاء الاصطناعي ثانتين).</span>
                    </li>
                </ul>
            </div>
            <button onclick="openDetailModal('modal-2')" class="mt-6 w-full py-2.5 bg-cyan-500/10 hover:bg-cyan-500 hover:text-slate-950 text-cyan-glow font-bold text-xs rounded-xl border border-cyan-500/30 transition-all flex items-center justify-center gap-2">
                <span>عرض التفاصيل الكاملة</span>
                <i class="fa-solid fa-arrow-left"></i>
            </button>
        </div>

        <!-- DIAGRAM 3: FINTECH HOLOGRAM WRISTBAND -->
        <div class="diagram-card glass-panel glass-panel-hover rounded-2xl p-6 flex flex-col justify-between transition-all duration-300" data-category="wristband">
            <div>
                <div class="flex items-center justify-between mb-4">
                    <span class="text-xs font-mono font-bold text-cyan-glow bg-cyan-950/80 px-3 py-1 rounded-full border border-cyan-500/30">رسم (3)</span>
                    <div class="w-10 h-10 rounded-xl bg-cyan-500/10 text-cyan-glow flex items-center justify-center text-lg">
                        <i class="fa-solid fa-stopwatch-20"></i>
                    </div>
                </div>
                <h3 class="text-xl font-bold text-white mb-2">سوار الهولوجرام المالي</h3>
                <p class="text-xs text-gray-400 leading-relaxed mb-4">عرض مرئي هولوجرامي مدمج على المعصم لتوضيح الرصيد، البيانات، وعرض المؤشرات الحيوية.</p>

                <ul class="space-y-2 text-xs text-gray-300">
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-chart-line text-cyan-400"></i>
                        <span>عروض الهولوجرام المالي والتنبؤ الحسابي.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-chart-pie text-cyan-400"></i>
                        <span>عرض المؤشرات الحيوية والمالية والائتمانية.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-file-invoice text-cyan-400"></i>
                        <span>توضيح المستندات والرصيد والرسومات البيانية.</span>
                    </li>
                </ul>
            </div>
            <button onclick="openDetailModal('modal-3')" class="mt-6 w-full py-2.5 bg-cyan-500/10 hover:bg-cyan-500 hover:text-slate-950 text-cyan-glow font-bold text-xs rounded-xl border border-cyan-500/30 transition-all flex items-center justify-center gap-2">
                <span>عرض التفاصيل الكاملة</span>
                <i class="fa-solid fa-arrow-left"></i>
            </button>
        </div>

        <!-- DIAGRAM 4: SMART VAULTS & CONTRACTS -->
        <div class="diagram-card glass-panel glass-panel-hover rounded-2xl p-6 flex flex-col justify-between transition-all duration-300" data-category="vaults">
            <div>
                <div class="flex items-center justify-between mb-4">
                    <span class="text-xs font-mono font-bold text-cyan-glow bg-cyan-950/80 px-3 py-1 rounded-full border border-cyan-500/30">رسم (4)</span>
                    <div class="w-10 h-10 rounded-xl bg-cyan-500/10 text-cyan-glow flex items-center justify-center text-lg">
                        <i class="fa-solid fa-cubes"></i>
                    </div>
                </div>
                <h3 class="text-xl font-bold text-white mb-2">نظام الخزائن والعقود الذكية</h3>
                <p class="text-xs text-gray-400 leading-relaxed mb-4">الاقتصاد المجتمعي، التمويل اللامركزي، وإدارة التوريث والتركة تلقائياً بشروط مبرمجة.</p>

                <ul class="space-y-2 text-xs text-gray-300">
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-network-wired text-cyan-400"></i>
                        <span>مجمعات التمويل التخطيطي اللامركزي.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-vault text-cyan-400"></i>
                        <span>إدارة الورثة خزائن التوريث الرقمي الآلي.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-file-contract text-cyan-400"></i>
                        <span>تحقق شروط مبرمجة (وفاة، بلوغ سن).</span>
                    </li>
                </ul>
            </div>
            <button onclick="openDetailModal('modal-4')" class="mt-6 w-full py-2.5 bg-cyan-500/10 hover:bg-cyan-500 hover:text-slate-950 text-cyan-glow font-bold text-xs rounded-xl border border-cyan-500/30 transition-all flex items-center justify-center gap-2">
                <span>عرض التفاصيل الكاملة</span>
                <i class="fa-solid fa-arrow-left"></i>
            </button>
        </div>

        <!-- DIAGRAM 5: SMART CONNECTED KITCHEN -->
        <div class="diagram-card glass-panel glass-panel-hover rounded-2xl p-6 flex flex-col justify-between transition-all duration-300" data-category="kitchen">
            <div>
                <div class="flex items-center justify-between mb-4">
                    <span class="text-xs font-mono font-bold text-cyan-glow bg-cyan-950/80 px-3 py-1 rounded-full border border-cyan-500/30">رسم (5)</span>
                    <div class="w-10 h-10 rounded-xl bg-cyan-500/10 text-cyan-glow flex items-center justify-center text-lg">
                        <i class="fa-solid fa-robot"></i>
                    </div>
                </div>
                <h3 class="text-xl font-bold text-white mb-2">المطبخ الذكي والمال القابل للبرمجة</h3>
                <p class="text-xs text-gray-400 leading-relaxed mb-4">إنترنت الأشياء المدمج بالمطبخ، دفع ذاتي وتواصل مباشر بين روبوت المطبخ والمتاجر.</p>

                <ul class="space-y-2 text-xs text-gray-300">
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-utensils text-cyan-400"></i>
                        <span>روبوت مطبخ متصل بالمتجر لتلبية الاحتياجات.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-kitchen-set text-cyan-400"></i>
                        <span>ثلاجة ذكية تحدد النواقص تلقائياً.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-coins text-cyan-400"></i>
                        <span>الدفع الذاتي بالنواقص عبر المال القابل للبرمجة.</span>
                    </li>
                </ul>
            </div>
            <button onclick="openDetailModal('modal-5')" class="mt-6 w-full py-2.5 bg-cyan-500/10 hover:bg-cyan-500 hover:text-slate-950 text-cyan-glow font-bold text-xs rounded-xl border border-cyan-500/30 transition-all flex items-center justify-center gap-2">
                <span>عرض التفاصيل الكاملة</span>
                <i class="fa-solid fa-arrow-left"></i>
            </button>
        </div>

        <!-- DIAGRAM 6: INTEGRATED CRYSTAL VAULTS -->
        <div class="diagram-card glass-panel glass-panel-hover rounded-2xl p-6 flex flex-col justify-between transition-all duration-300" data-category="crystal">
            <div>
                <div class="flex items-center justify-between mb-4">
                    <span class="text-xs font-mono font-bold text-cyan-glow bg-cyan-950/80 px-3 py-1 rounded-full border border-cyan-500/30">رسم (6)</span>
                    <div class="w-10 h-10 rounded-xl bg-cyan-500/10 text-cyan-glow flex items-center justify-center text-lg">
                        <i class="fa-solid fa-gem"></i>
                    </div>
                </div>
                <h3 class="text-xl font-bold text-white mb-2">شبكة الخزائن والكاش الكريستالي</h3>
                <p class="text-xs text-gray-400 leading-relaxed mb-4">دمج الخزائن السحابية والفيزيائية مع المحفظة الكريستالية المحمولة لحفظ الأصول.</p>

                <ul class="space-y-2 text-xs text-gray-300">
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-box-archive text-cyan-400"></i>
                        <span>الكاش الكريستالي (المحمول) للتحويل الفوري.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-cloud text-cyan-400"></i>
                        <span>خزائن سحابية مخصصة لحفظ الأصول.</span>
                    </li>
                    <li class="flex items-center gap-2">
                        <i class="fa-solid fa-box text-cyan-400"></i>
                        <span>خزائن مادية مشفرة ومؤمنة حيوياً.</span>
                    </li>
                </ul>
            </div>
            <button onclick="openDetailModal('modal-6')" class="mt-6 w-full py-2.5 bg-cyan-500/10 hover:bg-cyan-500 hover:text-slate-950 text-cyan-glow font-bold text-xs rounded-xl border border-cyan-500/30 transition-all flex items-center justify-center gap-2">
                <span>عرض التفاصيل الكاملة</span>
                <i class="fa-solid fa-arrow-left"></i>
            </button>
        </div>

    </div>
</main>

<!-- FOOTER SECTION -->
<footer class="relative z-10 border-t border-cyan-500/20 bg-space-950 py-8 mt-12 text-center text-xs text-gray-400">
    <div class="max-w-7xl mx-auto px-4 flex flex-col sm:flex-row items-center justify-between gap-4">
        <div class="flex items-center space-x-2 space-x-reverse">
            <span class="font-bold text-white">مشروع مدار MIDAR</span>
            <span>- المعرض المدرسي 2026</span>
        </div>
        <p>تم تطوير هذه البوابة لعرض جميع الرسوم الهيكلية المعتمدة لمشروع مدار الذكي</p>
        <button onclick="openModal('feedbackModal')" class="text-cyan-glow underline hover:text-white">
            ترك تقييم وانطباع الحضور
        </button>
    </div>
</footer>

<!-- MODALS FOR DETAILED VIEW OF EACH DIAGRAM -->

<!-- MODAL 1 -->
<div id="modal-1" class="fixed inset-0 z-50 bg-black/85 backdrop-blur-lg hidden flex items-center justify-center p-4">
    <div class="glass-panel w-full max-w-2xl rounded-2xl p-6 max-h-[90vh] overflow-y-auto border border-cyan-500/40">
        <div class="flex justify-between items-center pb-4 border-b border-gray-800">
            <h3 class="text-lg font-bold text-white flex items-center gap-2">
                <i class="fa-solid fa-glasses text-cyan-glow"></i>
                رسم (1) - الأجهزة القابلة للارتداء وسائط التحقق والهوية البيولوجية
            </h3>
            <button onclick="closeDetailModal('modal-1')" class="text-gray-400 hover:text-white text-xl p-2"><i class="fa-solid fa-xmark"></i></button>
        </div>
        <div class="py-4 space-y-4 text-sm text-gray-300">
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">1. وسائط التحقق ولهوية البيولوجية</h4>
                <p class="text-xs text-gray-400">إلغاء الصرافات والفروع التقليدية بالكامل، وإلغاء البطاقات البلاستيكية والاستعاضة عنها بالوسائط المدمجة.</p>
            </div>
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">1b. خيارات الدفع المستقبلية</h4>
                <p class="text-xs text-gray-400">زرع شريحة إلكترونية متطورة تحت الجلد لإتمام الدفع البيومتري في أجزاء من الثانية.</p>
            </div>
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">1c. التعرف الحركي والصوتي</h4>
                <p class="text-xs text-gray-400">مطابقة الهوية بناءً على نبرة الصوت الفريدة، بالإضافة إلى تحليل بنية مشية المستخدم لضمان أعلى مستويات الأمان.</p>
            </div>
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">1d. النظارات والعدسات والتوقيع المشفر</h4>
                <p class="text-xs text-gray-400">نظارات الواقع الممتد (XR) والعدسات اللاصقة، بالإضافة للتوقيع المشفر المباشر في الهواء (Secure Blockchain Signature).</p>
            </div>
        </div>
    </div>
</div>

<!-- MODAL 2 -->
<div id="modal-2" class="fixed inset-0 z-50 bg-black/85 backdrop-blur-lg hidden flex items-center justify-center p-4">
    <div class="glass-panel w-full max-w-2xl rounded-2xl p-6 max-h-[90vh] overflow-y-auto border border-cyan-500/40">
        <div class="flex justify-between items-center pb-4 border-b border-gray-800">
            <h3 class="text-lg font-bold text-white flex items-center gap-2">
                <i class="fa-solid fa-capsules text-cyan-glow"></i>
                رسم (2) - كبسولة التحليل البيومتري البنك التنبؤي ومستشار المشاعر
            </h3>
            <button onclick="closeDetailModal('modal-2')" class="text-gray-400 hover:text-white text-xl p-2"><i class="fa-solid fa-xmark"></i></button>
        </div>
        <div class="py-4 space-y-4 text-sm text-gray-300">
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">2a & 2b. كبسولة التحليل ومستشار المشاعر اللحظية</h4>
                <p class="text-xs text-gray-400">مصادقة المؤشرات الحيوية كنبض القلب، مع خاصية تنبيه حماية المستخدم ووقف العمليات المالية مؤقتاً عند رصد عدم الاتزان النفسي أو التوتر.</p>
            </div>
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">2c. التوأم المالي الرقمي</h4>
                <p class="text-xs text-gray-400">محاكاة افتراضية دقيقة لنتائج القرارات المالية المستقبلية قبل اتخاذها لتجنب الخسائر.</p>
            </div>
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">2d. زمن انتظار صفر (Zero Wait-Time)</h4>
                <p class="text-xs text-gray-400">تحليل الذكاء الاصطناعي الفوري وعرض الحلول والتوصيات خلال ثانيتين فقط.</p>
            </div>
        </div>
    </div>
</div>

<!-- MODAL 3 -->
<div id="modal-3" class="fixed inset-0 z-50 bg-black/85 backdrop-blur-lg hidden flex items-center justify-center p-4">
    <div class="glass-panel w-full max-w-2xl rounded-2xl p-6 max-h-[90vh] overflow-y-auto border border-cyan-500/40">
        <div class="flex justify-between items-center pb-4 border-b border-gray-800">
            <h3 class="text-lg font-bold text-white flex items-center gap-2">
                <i class="fa-solid fa-stopwatch-20 text-cyan-glow"></i>
                رسم (3) - سوار الهولوجرام المالي
            </h3>
            <button onclick="closeDetailModal('modal-3')" class="text-gray-400 hover:text-white text-xl p-2"><i class="fa-solid fa-xmark"></i></button>
        </div>
        <div class="py-4 space-y-4 text-sm text-gray-300">
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">عرض الهولوجرام المالي المباشر</h4>
                <p class="text-xs text-gray-400">إسقاط ثلاثي الأبعاد مرئي يعرض المؤشرات الحيوية، الحالة المالية والائتمانية، وتوضيح المستندات الحية وحالة الرصيد بوضوح فوق المعصم.</p>
            </div>
        </div>
    </div>
</div>

<!-- MODAL 4 -->
<div id="modal-4" class="fixed inset-0 z-50 bg-black/85 backdrop-blur-lg hidden flex items-center justify-center p-4">
    <div class="glass-panel w-full max-w-2xl rounded-2xl p-6 max-h-[90vh] overflow-y-auto border border-cyan-500/40">
        <div class="flex justify-between items-center pb-4 border-b border-gray-800">
            <h3 class="text-lg font-bold text-white flex items-center gap-2">
                <i class="fa-solid fa-cubes text-cyan-glow"></i>
                رسم (4) - نظام الخزائن التخطيطية والاقتصاد المجتمعي والعقود الذكية
            </h3>
            <button onclick="closeDetailModal('modal-4')" class="text-gray-400 hover:text-white text-xl p-2"><i class="fa-solid fa-xmark"></i></button>
        </div>
        <div class="py-4 space-y-4 text-sm text-gray-300">
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">التمويل اللامركزي والتوريث الذكي</h4>
                <p class="text-xs text-gray-400">مجمعات تمويل تخطيطية لامركزية، وتمرير التركة والأصول للورثة تلقائياً عبر خزائن التوريث الرقمي عند تحقق شروط مبرمجة مسبقاً (مثل الوفاة أو بلوغ سن معين).</p>
            </div>
        </div>
    </div>
</div>

<!-- MODAL 5 -->
<div id="modal-5" class="fixed inset-0 z-50 bg-black/85 backdrop-blur-lg hidden flex items-center justify-center p-4">
    <div class="glass-panel w-full max-w-2xl rounded-2xl p-6 max-h-[90vh] overflow-y-auto border border-cyan-500/40">
        <div class="flex justify-between items-center pb-4 border-b border-gray-800">
            <h3 class="text-lg font-bold text-white flex items-center gap-2">
                <i class="fa-solid fa-robot text-cyan-glow"></i>
                رسم (5) - المطبخ الذكي المتصل وإنترنت الأشياء والمال القابل للبرمجة
            </h3>
            <button onclick="closeDetailModal('modal-5')" class="text-gray-400 hover:text-white text-xl p-2"><i class="fa-solid fa-xmark"></i></button>
        </div>
        <div class="py-4 space-y-4 text-sm text-gray-300">
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">الإنترنت المدمج والدفع الذاتي للنواقص</h4>
                <p class="text-xs text-gray-400">روبوت مطبخ وثلاجة ذكية متصلان مباشرة بالمتجر، يتم الدفع الذاتي التلقائي للنواقص المنزلية عبر محفظة المال القابل للبرمجة.</p>
            </div>
        </div>
    </div>
</div>

<!-- MODAL 6 -->
<div id="modal-6" class="fixed inset-0 z-50 bg-black/85 backdrop-blur-lg hidden flex items-center justify-center p-4">
    <div class="glass-panel w-full max-w-2xl rounded-2xl p-6 max-h-[90vh] overflow-y-auto border border-cyan-500/40">
        <div class="flex justify-between items-center pb-4 border-b border-gray-800">
            <h3 class="text-lg font-bold text-white flex items-center gap-2">
                <i class="fa-solid fa-gem text-cyan-glow"></i>
                رسم (6) - شبكة الخزائن المتكاملة والكاش الكريستالي
            </h3>
            <button onclick="closeDetailModal('modal-6')" class="text-gray-400 hover:text-white text-xl p-2"><i class="fa-solid fa-xmark"></i></button>
        </div>
        <div class="py-4 space-y-4 text-sm text-gray-300">
            <div class="p-3 bg-space-900 rounded-xl border border-cyan-500/20">
                <h4 class="font-bold text-cyan-glow mb-1">الكاش الكريستالي والخزائن الفيزيائية</h4>
                <p class="text-xs text-gray-400">الكاش الكريستالي المحمول للعمليات الفورية، مع دمج الخزائن السحابية والمادية للحفاظ على الأصول وتوفير حماية وتشفير حيوية فائقة.</p>
            </div>
        </div>
    </div>
</div>

<!-- FEEDBACK FORM MODAL -->
<div id="feedbackModal" class="fixed inset-0 z-50 bg-black/85 backdrop-blur-lg hidden flex items-center justify-center p-4">
    <div class="glass-panel w-full max-w-lg rounded-2xl overflow-hidden border border-cyan-500/40">
        <div class="p-4 border-b border-gray-800 flex justify-between items-center bg-space-900">
            <h3 class="text-lg font-bold text-white flex items-center gap-2">
                <i class="fa-solid fa-star-half-stroke text-cyan-glow"></i>
                استبيان وتقييم عرض مشروع مدار
            </h3>
            <button onclick="closeModal('feedbackModal')" class="text-gray-400 hover:text-white text-xl p-2"><i class="fa-solid fa-xmark"></i></button>
        </div>
        <form id="feedbackForm" onsubmit="submitFeedback(event)" class="p-6 space-y-4">
            <div>
                <label class="block text-xs font-semibold text-gray-300 mb-2 text-center">ما تقييمكم العام لابتكار مشروع "مدار" والمعروضات؟</label>
                <div class="star-rating flex justify-center space-x-3 space-x-reverse text-3xl text-gray-600 py-2">
                    <i class="fa-solid fa-star" onclick="setRating(1)"></i>
                    <i class="fa-solid fa-star" onclick="setRating(2)"></i>
                    <i class="fa-solid fa-star" onclick="setRating(3)"></i>
                    <i class="fa-solid fa-star" onclick="setRating(4)"></i>
                    <i class="fa-solid fa-star" onclick="setRating(5)"></i>
                </div>
            </div>

            <div>
                <label class="block text-xs font-semibold text-gray-300 mb-1">الاسم الكريم (اختياري)</label>
                <input type="text" placeholder="أدخل اسمك..." class="w-full p-3 bg-space-900 rounded-xl border border-gray-700 text-white text-sm focus:border-cyan-glow focus:outline-none">
            </div>

            <div>
                <label class="block text-xs font-semibold text-gray-300 mb-1">ملاحظاتكم وانطباعاتكم عن المشروع</label>
                <textarea rows="3" required placeholder="اكتب رأيك الثمين حول المشروع..." class="w-full p-3 bg-space-900 rounded-xl border border-gray-700 text-white text-sm focus:border-cyan-glow focus:outline-none"></textarea>
            </div>

            <button type="submit" class="w-full py-3 bg-gradient-to-r from-cyan-400 to-blue-600 text-slate-950 font-bold rounded-xl hover:opacity-90 transition-opacity">
                إرسال التقييم
            </button>
        </form>
    </div>
</div>

<!-- TOAST NOTIFICATION -->
<div id="toast" class="fixed bottom-6 left-1/2 transform -translate-x-1/2 z-50 bg-cyan-950 border border-cyan-400 text-cyan-glow px-6 py-3 rounded-xl shadow-2xl hidden flex items-center space-x-3 space-x-reverse">
    <i class="fa-solid fa-circle-check text-cyan-400 text-lg"></i>
    <span id="toastMsg" class="text-sm font-semibold text-white"></span>
</div>

<script>
    function filterComponents(category) {
        const cards = document.querySelectorAll('.diagram-card');
        const btns = document.querySelectorAll('.tab-btn');

        btns.forEach(btn => {
            btn.classList.remove('bg-cyan-500', 'text-black', 'shadow-[0_0_15px_rgba(0,240,255,0.4)]');
            btn.classList.add('bg-space-800', 'text-gray-300');
        });

        const activeBtn = document.getElementById(`tab-${category}`);
        if (activeBtn) {
            activeBtn.classList.remove('bg-space-800', 'text-gray-300');
            activeBtn.classList.add('bg-cyan-500', 'text-black', 'shadow-[0_0_15px_rgba(0,240,255,0.4)]');
        }

        cards.forEach(card => {
            if (category === 'all' || card.dataset.category === category) {
                card.style.display = 'flex';
            } else {
                card.style.display = 'none';
            }
        });
    }

    function openDetailModal(id) {
        document.getElementById(id).classList.remove('hidden');
    }

    function closeDetailModal(id) {
        document.getElementById(id).classList.add('hidden');
    }

    function openModal(id) {
        document.getElementById(id).classList.remove('hidden');
    }

    function closeModal(id) {
        document.getElementById(id).classList.add('hidden');
    }

    function setRating(rating) {
        const stars = document.querySelectorAll('.star-rating i');
        stars.forEach((star, index) => {
            if (index < rating) {
                star.classList.remove('text-gray-600');
                star.classList.add('text-yellow-400');
            } else {
                star.classList.remove('text-yellow-400');
                star.classList.add('text-gray-600');
            }
        });
    }

    function submitFeedback(e) {
        e.preventDefault();
        closeModal('feedbackModal');
        showToast('تم استلام تقييمك بنجاح! شكراً لدعمك مشروع مدار 🚀');
        document.getElementById('feedbackForm').reset();
        setRating(0);
    }

    function showToast(msg) {
        const toast = document.getElementById('toast');
        document.getElementById('toastMsg').innerText = msg;
        toast.classList.remove('hidden');
        setTimeout(() => {
            toast.classList.add('hidden');
        }, 3500);
    }
</script>
</body>
</html>

