<!DOCTYPE html>
<html lang="th" class="h-full">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>iPhone 14 Plus - Personal Color Ecosystem (Liquid Glass Edition)</title>
    
    <!-- Google Fonts: Kanit (Thai) & Inter (English) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Kanit:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'sandy-cream': '#EAE4DC',
                        'sandy-cream-dark': '#E3DDD4',
                        'liquid-purple-start': '#9B62FF',
                        'liquid-purple-end': '#6836E8',
                        'liquid-teal-start': '#42E3C2',
                        'liquid-teal-end': '#0BBDA5',
                        'obsidian': '#1C1C1E',
                    },
                    fontFamily: {
                        sans: ['Inter', 'Kanit', 'sans-serif'],
                        thai: ['Kanit', 'sans-serif'],
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Scrollbar for App Viewport */
        .app-scroll::-webkit-scrollbar {
            width: 0px;
            background: transparent;
        }
        .app-scroll {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }

        /* 1. LIQUID GLASS SURFACES */
        .liquid-glass {
            background: rgba(255, 255, 255, 0.45);
            backdrop-filter: blur(24px) saturate(180%);
            -webkit-backdrop-filter: blur(24px) saturate(180%);
            border: 1px solid rgba(255, 255, 255, 0.8);
            box-shadow: 
                0 10px 30px -5px rgba(180, 170, 160, 0.25),
                0 4px 12px 0 rgba(0, 0, 0, 0.03),
                inset 0 1px 2px 0 rgba(255, 255, 255, 0.95),
                inset 0 -1px 2px 0 rgba(0, 0, 0, 0.03);
            position: relative;
        }

        /* Glass Specular Reflection Highlight Overlay */
        .liquid-glass::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 45%;
            background: linear-gradient(180deg, rgba(255, 255, 255, 0.5) 0%, rgba(255, 255, 255, 0) 100%);
            border-top-left-radius: inherit;
            border-top-right-radius: inherit;
            pointer-events: none;
        }

        /* 2. IRIDESCENT AURORA GLASS CARD */
        .aurora-glass {
            background: linear-gradient(135deg, rgba(255, 200, 210, 0.55), rgba(210, 180, 255, 0.55), rgba(160, 230, 255, 0.55));
            backdrop-filter: blur(28px) saturate(200%);
            -webkit-backdrop-filter: blur(28px) saturate(200%);
            border: 1px solid rgba(255, 255, 255, 0.9);
            box-shadow: 
                0 15px 35px -5px rgba(190, 150, 220, 0.35),
                0 0 25px 2px rgba(255, 255, 255, 0.6),
                inset 0 1.5px 3px 0 rgba(255, 255, 255, 0.95);
            position: relative;
            overflow: hidden;
        }

        .aurora-glass::after {
            content: '';
            position: absolute;
            -inset: 100%;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.4) 0%, transparent 60%);
            animation: rotate-aurora 12s linear infinite;
            pointer-events: none;
        }

        @keyframes rotate-aurora {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* 3. GLOSSY PILL BUTTONS (CTA & PILLS) */
        .pill-cta-purple {
            background: linear-gradient(180deg, #9B62FF 0%, #6836E8 100%);
            border-radius: 999px;
            box-shadow: 
                0 8px 20px -3px rgba(120, 50, 235, 0.45),
                inset 0 2px 3px 0 rgba(255, 255, 255, 0.7),
                inset 0 -2px 4px 0 rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
            transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .pill-cta-purple::before {
            content: '';
            position: absolute;
            top: 2px;
            left: 10px;
            right: 10px;
            height: 35%;
            background: rgba(255, 255, 255, 0.45);
            border-radius: 999px;
            pointer-events: none;
        }

        .pill-cta-teal {
            background: linear-gradient(180deg, #42E3C2 0%, #0BBDA5 100%);
            border-radius: 999px;
            box-shadow: 
                0 8px 20px -3px rgba(11, 189, 165, 0.4),
                inset 0 2px 3px 0 rgba(255, 255, 255, 0.8),
                inset 0 -2px 4px 0 rgba(0, 0, 0, 0.15);
            position: relative;
            overflow: hidden;
            transition: all 0.2s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .pill-cta-teal::before {
            content: '';
            position: absolute;
            top: 2px;
            left: 10px;
            right: 10px;
            height: 35%;
            background: rgba(255, 255, 255, 0.5);
            border-radius: 999px;
            pointer-events: none;
        }

        /* PURE WHITE PILL SURFACES */
        .white-pill {
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 1);
            border-radius: 999px;
            box-shadow: 
                0 4px 15px rgba(0, 0, 0, 0.04),
                inset 0 1px 2px rgba(0, 0, 0, 0.03);
        }

        /* iPhone Metallic Frame Contour */
        .iphone-frame {
            box-shadow: 
                0 0 0 2px #2c2c2e,
                0 0 0 4px #1c1c1e,
                0 30px 70px -10px rgba(0, 0, 0, 0.65),
                0 0 90px rgba(155, 98, 255, 0.2);
        }

        /* Scanning Beam Animation */
        @keyframes scan-glow {
            0% { top: 0%; opacity: 0.8; }
            50% { opacity: 1; }
            100% { top: 100%; opacity: 0.8; }
        }

        .animate-scan {
            animation: scan-glow 2.2s ease-in-out infinite alternate;
        }
    </style>
</head>
<body class="bg-slate-950 text-slate-800 font-sans min-h-screen flex flex-col items-center justify-center p-2 sm:p-6 overflow-x-hidden selection:bg-purple-200">

    <!-- Desktop Presentation Bar -->
    <div class="mb-4 text-center z-10">
        <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-slate-900/90 border border-slate-800 text-slate-300 text-xs sm:text-sm font-medium backdrop-blur-md mb-1 shadow-xl">
            <span class="w-2.5 h-2.5 rounded-full bg-teal-400 animate-pulse"></span>
            <span>iPhone 14 Plus Interactive Prototype</span>
            <span class="text-slate-600">|</span>
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-teal-300 font-bold">Liquid Glass Kit</span>
        </div>
        <p class="text-slate-400 text-xs hidden sm:block">คลิกแท็บเมนูด้านล่างเพื่อสัมผัสการเปลี่ยนโหมด Interactive Liquid UI</p>
    </div>

    <!-- MAIN IPHONE 14 PLUS MOCKUP CONTAINER (428px x 880px) -->
    <div class="relative w-full max-w-[428px] h-[880px] bg-obsidian rounded-[52px] iphone-frame p-[12px] flex flex-col justify-between transition-all duration-300 transform scale-[0.88] sm:scale-100 origin-center select-none">
        
        <!-- iPhone Metallic Side Edge Highlight -->
        <div class="absolute -inset-[1px] rounded-[53px] border border-white/10 pointer-events-none"></div>

        <!-- INNER DISPLAY VIEWPORT (46px Border Radius) -->
        <div class="relative w-full h-full bg-[#EAE4DC] rounded-[42px] overflow-hidden flex flex-col justify-between shadow-inner border border-black/5">
            
            <!-- iOS Status Bar & Top Notch -->
            <div class="absolute top-0 left-0 right-0 h-11 z-50 flex items-center justify-between px-7 pt-1 pointer-events-none">
                <!-- Live Clock -->
                <span id="ios-time" class="text-[13px] font-bold tracking-tight text-slate-800">09:41</span>
                
                <!-- Notch / Dynamic Camera Island -->
                <div class="absolute top-0 left-1/2 -translate-x-1/2 w-[158px] h-[28px] bg-black rounded-b-[18px] flex items-center justify-center px-4 gap-3 z-50">
                    <div class="w-3 h-3 rounded-full bg-slate-900 border border-slate-800 flex items-center justify-center">
                        <div class="w-1.5 h-1.5 rounded-full bg-blue-950/60"></div>
                    </div>
                    <div class="w-2.5 h-2.5 rounded-full bg-slate-900 border border-slate-800 flex items-center justify-center">
                        <div class="w-1 h-1 rounded-full bg-emerald-950/50"></div>
                    </div>
                    <div class="w-12 h-1 bg-slate-900/80 rounded-full"></div>
                </div>

                <!-- Icons (Signal, Wifi, Battery) -->
                <div class="flex items-center gap-1.5 text-slate-800 text-xs">
                    <i class="fa-solid fa-signal text-[10px]"></i>
                    <i class="fa-solid fa-wifi text-[10px]"></i>
                    <div class="w-5 h-2.5 border border-slate-800 rounded-sm p-0.5 flex items-center">
                        <div class="h-full w-full bg-slate-800 rounded-[1px]"></div>
                    </div>
                </div>
            </div>

            <!-- APP SCROLLABLE VIEWPORT AREA -->
            <div id="app-viewport" class="w-full h-full pt-12 pb-24 overflow-y-auto app-scroll relative">

                <!-- ==================== TAB 1: HOME (DASHBOARD) ==================== -->
                <section id="tab-home" class="p-4 space-y-4 animate-fade-in">
                    
                    <!-- Profile Header Bar -->
                    <div class="flex items-center justify-between pt-1">
                        <div class="flex items-center gap-3">
                            <div class="relative">
                                <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=150&q=80" 
                                     alt="Profile Avatar" 
                                     class="w-12 h-12 rounded-full object-cover border-2 border-white/90 shadow-md"
                                     onerror="this.src='https://placehold.co/150x150/FFC0CB/ffffff?text=Nalin'">
                                <div class="absolute -bottom-1 -right-1 bg-gradient-to-r from-purple-500 to-indigo-500 text-white text-[8px] font-extrabold px-1.5 py-0.5 rounded-full border border-white shadow-sm">
                                    PRO
                                </div>
                            </div>
                            <div>
                                <div class="text-[11px] text-slate-500 font-medium">ยินดีต้อนรับกลับค่ะ 🌸</div>
                                <h2 class="text-base font-bold text-slate-900 leading-tight">คุณนลิน พรประเสริฐ</h2>
                            </div>
                        </div>

                        <button onclick="showToast('การแจ้งเตือนล่าสุด: 2 รายการ')" class="w-10 h-10 white-pill flex items-center justify-center text-slate-700 shadow-sm active:scale-95 transition">
                            <i class="fa-regular fa-bell text-sm"></i>
                        </button>
                    </div>

                    <!-- 16-Season Iridescent Aurora Glass Card -->
                    <div class="aurora-glass rounded-[28px] p-5 shadow-xl relative">
                        <div class="flex items-center justify-between mb-3">
                            <span class="px-3 py-1 rounded-full bg-white/70 text-purple-900 text-[10px] font-bold border border-white/80 shadow-xs backdrop-blur-md">
                                <i class="fa-solid fa-sparkles mr-1 text-purple-600"></i> PERSONAL COLOR
                            </span>
                            <span class="text-[10px] font-extrabold text-slate-800 bg-white/50 px-2.5 py-0.5 rounded-full border border-white/60">
                                16-SEASON SYSTEM
                            </span>
                        </div>

                        <div class="mb-4">
                            <div class="text-xs font-semibold text-slate-700">ผลการวิเคราะห์หลัก</div>
                            <h3 class="text-2xl font-extrabold text-slate-900 tracking-wide mt-0.5">LIGHT SUMMER</h3>
                            <p class="text-xs text-slate-600 mt-1 leading-relaxed">
                                โทนสีเย็น นุ่มนวล สว่าง (Cool, Soft & Light Palette) ขับประกายออร่าอย่างเป็นธรรมชาติ
                            </p>
                        </div>

                        <!-- Swatch Dots in White Pill Container -->
                        <div class="white-pill p-2.5 flex items-center justify-between gap-2">
                            <div class="flex items-center gap-2">
                                <div class="w-8 h-8 rounded-full bg-[#B0E0E6] shadow-sm border-2 border-white flex items-center justify-center text-[9px] font-bold text-slate-700" title="Powder Blue">#B0</div>
                                <div class="w-8 h-8 rounded-full bg-[#FFC0CB] shadow-sm border-2 border-white flex items-center justify-center text-[9px] font-bold text-slate-700" title="Rose Pink">#FF</div>
                                <div class="w-8 h-8 rounded-full bg-[#E6E6FA] shadow-sm border-2 border-white flex items-center justify-center text-[9px] font-bold text-slate-700" title="Lavender">#E6</div>
                                <div class="w-8 h-8 rounded-full bg-[#D8BFD8] shadow-sm border-2 border-white flex items-center justify-center text-[9px] font-bold text-slate-700" title="Thistle">#D8</div>
                            </div>
                            <button onclick="navigateTo('tab-wardrobe')" class="pill-cta-purple px-3.5 py-1.5 text-white text-xs font-bold flex items-center gap-1 active:scale-95">
                                <span>จานสี</span>
                                <i class="fa-solid fa-chevron-right text-[9px]"></i>
                            </button>
                        </div>
                    </div>

                    <!-- White Pill Search Bar -->
                    <div class="white-pill px-4 py-2.5 flex items-center gap-3">
                        <i class="fa-solid fa-magnifying-glass text-slate-400 text-xs"></i>
                        <input type="text" placeholder="ค้นหาเฉดสี ลิปสติก หรือเสื้อผ้า..." class="bg-transparent text-xs text-slate-800 focus:outline-none w-full placeholder-slate-400">
                        <i class="fa-solid fa-sliders text-purple-600 text-xs"></i>
                    </div>

                    <!-- Shortcut Grid with Glossy Purple & Teal Jelly Buttons -->
                    <div>
                        <h4 class="text-xs font-bold text-slate-800 mb-2.5 px-1">ทางลัดประมวลผล Liquid Apps</h4>
                        <div class="grid grid-cols-3 gap-2.5">
                            <button onclick="navigateTo('tab-scanner')" class="liquid-glass p-3 rounded-2xl flex flex-col items-center text-center hover:scale-[1.02] transition active:scale-95">
                                <div class="w-11 h-11 pill-cta-purple flex items-center justify-center text-white text-base shadow-md mb-2">
                                    <i class="fa-solid fa-camera-retro"></i>
                                </div>
                                <span class="text-xs font-bold text-slate-800">สแกนสีผิว</span>
                                <span class="text-[9px] text-slate-500 mt-0.5">AI Diagnostic</span>
                            </button>

                            <button onclick="navigateTo('tab-beauty')" class="liquid-glass p-3 rounded-2xl flex flex-col items-center text-center hover:scale-[1.02] transition active:scale-95">
                                <div class="w-11 h-11 pill-cta-teal flex items-center justify-center text-white text-base shadow-md mb-2">
                                    <i class="fa-solid fa-wand-magic-sparkles"></i>
                                </div>
                                <span class="text-xs font-bold text-slate-800">ลองลิปสติก</span>
                                <span class="text-[9px] text-slate-500 mt-0.5">AR Try-On</span>
                            </button>

                            <button onclick="navigateTo('tab-wardrobe')" class="liquid-glass p-3 rounded-2xl flex flex-col items-center text-center hover:scale-[1.02] transition active:scale-95">
                                <div class="w-11 h-11 pill-cta-purple flex items-center justify-center text-white text-base shadow-md mb-2">
                                    <i class="fa-solid fa-shirt"></i>
                                </div>
                                <span class="text-xs font-bold text-slate-800">แมตช์ชุด</span>
                                <span class="text-[9px] text-slate-500 mt-0.5">Outfit Match</span>
                            </button>
                        </div>
                    </div>

                    <!-- Daily Color Recommendation Liquid Card -->
                    <div class="liquid-glass rounded-2xl p-4 space-y-3">
                        <div class="flex items-center justify-between">
                            <div class="flex items-center gap-2">
                                <span class="w-2 h-2 rounded-full bg-emerald-500"></span>
                                <h4 class="text-xs font-bold text-slate-900">แนะนำชุดแต่งกายประจำวัน</h4>
                            </div>
                            <span class="text-[10px] font-extrabold text-purple-700 bg-purple-100/80 px-2 py-0.5 rounded-full">
                                98% HARMONY
                            </span>
                        </div>
                        <p class="text-xs text-slate-600 leading-relaxed">
                            วันนี้เน้นการจับคู่เสื้อสี <strong class="text-sky-700">Powder Blue (#B0E0E6)</strong> เข้ากับกระโปรงสี <strong class="text-purple-700">Soft Lavender</strong> เพื่อลุคที่สะอาด สดใส น่าเชื่อถือ
                        </p>
                    </div>

                </section>

                <!-- ==================== TAB 2: SCANNER (AI DIAGNOSTICS) ==================== -->
                <section id="tab-scanner" class="p-4 space-y-4 hidden animate-fade-in">
                    
                    <div class="text-center pt-1">
                        <h2 class="text-base font-extrabold text-slate-900">AI Personal Color Diagnostics</h2>
                        <p class="text-[11px] text-slate-500">วิเคราะห์ undertone ผิว ความสว่าง และความเข้มของใบหน้า</p>
                    </div>

                    <!-- Glass Photo Upload & Preview Container -->
                    <div class="liquid-glass rounded-[28px] p-3 relative overflow-hidden flex flex-col items-center justify-center group">
                        
                        <!-- Photo Viewport Zone -->
                        <div class="relative w-full aspect-[4/5] rounded-2xl overflow-hidden shadow-inner">
                            <img id="scanner-preview-img" 
                                 src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=600&q=80" 
                                 alt="Scanner Face Preview" 
                                 class="w-full h-full object-cover transition-all duration-300">

                            <!-- Face Contour Frame Indicator -->
                            <div class="absolute inset-0 flex flex-col items-center justify-center pointer-events-none">
                                <div class="w-44 h-60 border-2 border-dashed border-white/90 rounded-[90px] flex items-center justify-center relative shadow-lg">
                                    <div class="absolute -top-3 px-2.5 py-0.5 white-pill text-purple-800 text-[9px] font-bold shadow-sm">
                                        จัดใบหน้าให้อยู่ในกรอบ
                                    </div>
                                    <!-- Dynamic points -->
                                    <div class="w-3 h-3 rounded-full bg-purple-400/80 border border-white animate-ping absolute top-1/3 left-6"></div>
                                    <div class="w-3 h-3 rounded-full bg-teal-400/80 border border-white animate-ping absolute top-1/2 right-6" style="animation-delay: 0.6s"></div>
                                </div>
                            </div>

                            <!-- Animated Scanning Beam -->
                            <div id="scan-beam" class="absolute inset-x-0 h-1.5 bg-gradient-to-r from-transparent via-purple-500 to-transparent shadow-[0_0_20px_#9B62FF] animate-scan hidden pointer-events-none"></div>
                        </div>

                        <!-- Sample Preset Selector Bar -->
                        <div class="w-full mt-2.5 flex items-center justify-between gap-1.5 px-1">
                            <span class="text-[10px] font-bold text-slate-600">ตัวอย่าง:</span>
                            <div class="flex gap-1.5">
                                <button onclick="changeScanPreset('cool')" class="px-2.5 py-1 white-pill text-[10px] font-semibold text-slate-700 hover:bg-white active:scale-95 transition">Cool Light</button>
                                <button onclick="changeScanPreset('warm')" class="px-2.5 py-1 white-pill text-[10px] font-semibold text-slate-700 hover:bg-white active:scale-95 transition">Warm Autumn</button>
                                <button onclick="changeScanPreset('spring')" class="px-2.5 py-1 white-pill text-[10px] font-semibold text-slate-700 hover:bg-white active:scale-95 transition">Spring</button>
                            </div>
                        </div>
                    </div>

                    <!-- Glossy Purple "ANALYZE NOW" CTA Button -->
                    <button id="btn-start-scan" onclick="runAIScan()" class="w-full py-3.5 pill-cta-purple text-white font-extrabold text-sm flex items-center justify-center gap-2 active:scale-95">
                        <i class="fa-solid fa-sparkles"></i>
                        <span>เริ่มวิเคราะห์สีผิว (ANALYZE NOW)</span>
                    </button>

                    <!-- Detailed Color Metrics Cards -->
                    <div id="scan-results-box" class="liquid-glass rounded-2xl p-4 space-y-3">
                        <div class="flex items-center justify-between border-b border-slate-200/60 pb-2.5">
                            <div>
                                <span class="text-[9px] text-purple-600 font-extrabold uppercase tracking-wider">AI Diagnostic Output</span>
                                <h3 id="res-season-title" class="text-sm font-extrabold text-slate-900">Light Summer (ฤดูร้อนโทนสว่าง)</h3>
                            </div>
                            <span class="px-2.5 py-1 pill-cta-teal text-white font-bold text-[10px]">
                                98.4% Match
                            </span>
                        </div>

                        <!-- 3 Metric Cards Grid -->
                        <div class="grid grid-cols-3 gap-2 text-center">
                            <div class="white-pill p-2 text-center">
                                <div class="text-[8px] text-slate-400 font-bold uppercase">UNDERTONE</div>
                                <div id="res-undertone" class="text-xs font-extrabold text-purple-600 mt-0.5">Cool Pink</div>
                            </div>
                            <div class="white-pill p-2 text-center">
                                <div class="text-[8px] text-slate-400 font-bold uppercase">BRIGHTNESS</div>
                                <div id="res-brightness" class="text-xs font-extrabold text-teal-600 mt-0.5">High Light</div>
                            </div>
                            <div class="white-pill p-2 text-center">
                                <div class="text-[8px] text-slate-400 font-bold uppercase">CONTRAST</div>
                                <div id="res-contrast" class="text-xs font-extrabold text-indigo-600 mt-0.5">Soft Low</div>
                            </div>
                        </div>

                        <!-- Best Swatches Row -->
                        <div>
                            <div class="text-[11px] font-bold text-slate-800 mb-1.5 flex items-center gap-1">
                                <i class="fa-solid fa-circle-check text-emerald-500"></i>
                                <span>เฉดสีขับผิวสูงสุด (Recommended Swatches)</span>
                            </div>
                            <div class="grid grid-cols-5 gap-1.5">
                                <div class="h-8 rounded-xl bg-[#B0E0E6] flex items-center justify-center text-[9px] font-bold text-slate-700 shadow-xs">#B0E</div>
                                <div class="h-8 rounded-xl bg-[#FFC0CB] flex items-center justify-center text-[9px] font-bold text-slate-700 shadow-xs">#FFC</div>
                                <div class="h-8 rounded-xl bg-[#E6E6FA] flex items-center justify-center text-[9px] font-bold text-slate-700 shadow-xs">#E6E</div>
                                <div class="h-8 rounded-xl bg-[#E0F8F1] flex items-center justify-center text-[9px] font-bold text-slate-700 shadow-xs">#E0F</div>
                                <div class="h-8 rounded-xl bg-[#D8BFD8] flex items-center justify-center text-[9px] font-bold text-slate-700 shadow-xs">#D8B</div>
                            </div>
                        </div>
                    </div>

                </section>

                <!-- ==================== TAB 3: WARDROBE (COLOR MATCHER) ==================== -->
                <section id="tab-wardrobe" class="p-4 space-y-4 hidden animate-fade-in">
                    
                    <div class="text-center pt-1">
                        <h2 class="text-base font-extrabold text-slate-900">Outfit Color Matcher</h2>
                        <p class="text-[11px] text-slate-500">จับคู่สีเสื้อผ้าและตรวจสอบเปอร์เซ็นต์ความเข้ากันได้</p>
                    </div>

                    <!-- Wardrobe Outfit Canvas Card -->
                    <div class="aurora-glass rounded-[28px] p-5 flex flex-col items-center justify-center relative">
                        
                        <!-- Garment Vector Canvas -->
                        <div class="w-36 h-56 relative flex flex-col items-center justify-center my-1">
                            <!-- Top Garment -->
                            <div id="garment-top" class="w-32 h-24 bg-[#B0E0E6] rounded-t-2xl rounded-b-lg shadow-md transition-all duration-300 relative flex items-center justify-center border border-white/60">
                                <span class="text-[9px] font-bold bg-white/80 px-2 py-0.5 rounded-full text-slate-700 shadow-xs">เสื้อท่อนบน</span>
                                <div class="absolute top-0 w-10 h-5 bg-sandy-cream rounded-b-full border-b border-slate-300/40"></div>
                            </div>
                            <!-- Bottom Garment -->
                            <div id="garment-bottom" class="w-28 h-28 bg-[#E6E6FA] rounded-b-2xl mt-1 shadow-md transition-all duration-300 relative flex items-center justify-center border border-white/60">
                                <span class="text-[9px] font-bold bg-white/80 px-2 py-0.5 rounded-full text-slate-700 shadow-xs">กระโปรง / กางเกง</span>
                            </div>
                        </div>

                        <!-- Match % Indicator Ring -->
                        <div class="w-full white-pill p-3 mt-2 flex items-center justify-around">
                            <div class="flex items-center gap-3">
                                <!-- Circular progress SVG -->
                                <div class="relative w-12 h-12 flex items-center justify-center">
                                    <svg class="w-12 h-12 transform -rotate-90">
                                        <circle cx="24" cy="24" r="20" stroke="#E2E8F0" stroke-width="4" fill="transparent"/>
                                        <circle id="match-ring" cx="24" cy="24" r="20" stroke="#9B62FF" stroke-width="4" stroke-dasharray="125.6" stroke-dashoffset="2.5" stroke-linecap="round" fill="transparent" class="transition-all duration-500"/>
                                    </svg>
                                    <span id="match-score-num" class="absolute text-xs font-extrabold text-purple-700">98%</span>
                                </div>
                                <div>
                                    <div class="text-[10px] text-slate-400 font-bold uppercase">HARMONY SCORE</div>
                                    <div id="match-advice-title" class="text-xs font-bold text-slate-800">Perfect Harmony</div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- White Pill Color Selection Bar Options -->
                    <div class="space-y-3">
                        <!-- Top Selection Pill Box -->
                        <div class="liquid-glass p-3 rounded-2xl space-y-2">
                            <div class="flex items-center justify-between text-xs font-bold text-slate-800">
                                <span>1. สีเสื้อท่อนบน (Top Garment)</span>
                                <span id="top-color-label" class="text-purple-700">Powder Blue</span>
                            </div>
                            <div class="grid grid-cols-6 gap-1.5">
                                <button onclick="setGarmentColor('top', '#B0E0E6', 'Powder Blue', 98)" class="w-full aspect-square rounded-full bg-[#B0E0E6] border-2 border-purple-500 shadow-xs"></button>
                                <button onclick="setGarmentColor('top', '#FFC0CB', 'Rose Pink', 96)" class="w-full aspect-square rounded-full bg-[#FFC0CB] border-2 border-white shadow-xs"></button>
                                <button onclick="setGarmentColor('top', '#E0F8F1', 'Soft Mint', 94)" class="w-full aspect-square rounded-full bg-[#E0F8F1] border-2 border-white shadow-xs"></button>
                                <button onclick="setGarmentColor('top', '#FFFFFF', 'Pure White', 90)" class="w-full aspect-square rounded-full bg-[#FFFFFF] border-2 border-slate-200 shadow-xs"></button>
                                <button onclick="setGarmentColor('top', '#FF4500', 'Vibrant Orange', 38)" class="w-full aspect-square rounded-full bg-[#FF4500] border-2 border-white shadow-xs"></button>
                                <button onclick="setGarmentColor('top', '#1A1A1A', 'Dark Obsidian', 52)" class="w-full aspect-square rounded-full bg-[#1A1A1A] border-2 border-white shadow-xs"></button>
                            </div>
                        </div>

                        <!-- Bottom Selection Pill Box -->
                        <div class="liquid-glass p-3 rounded-2xl space-y-2">
                            <div class="flex items-center justify-between text-xs font-bold text-slate-800">
                                <span>2. สีกางเกง/กระโปรง (Bottom Garment)</span>
                                <span id="bottom-color-label" class="text-teal-700">Soft Lavender</span>
                            </div>
                            <div class="grid grid-cols-6 gap-1.5">
                                <button onclick="setGarmentColor('bottom', '#E6E6FA', 'Soft Lavender', 98)" class="w-full aspect-square rounded-full bg-[#E6E6FA] border-2 border-teal-500 shadow-xs"></button>
                                <button onclick="setGarmentColor('bottom', '#D8BFD8', 'Plum Lavender', 95)" class="w-full aspect-square rounded-full bg-[#D8BFD8] border-2 border-white shadow-xs"></button>
                                <button onclick="setGarmentColor('bottom', '#6688A5', 'Dusty Blue', 92)" class="w-full aspect-square rounded-full bg-[#6688A5] border-2 border-white shadow-xs"></button>
                                <button onclick="setGarmentColor('bottom', '#F5F5DC', 'Soft Beige', 88)" class="w-full aspect-square rounded-full bg-[#F5F5DC] border-2 border-white shadow-xs"></button>
                                <button onclick="setGarmentColor('bottom', '#E5A000', 'Mustard Gold', 35)" class="w-full aspect-square rounded-full bg-[#E5A000] border-2 border-white shadow-xs"></button>
                                <button onclick="setGarmentColor('bottom', '#4A4A4A', 'Charcoal', 65)" class="w-full aspect-square rounded-full bg-[#4A4A4A] border-2 border-white shadow-xs"></button>
                            </div>
                        </div>
                    </div>

                </section>

                <!-- ==================== TAB 4: BEAUTY STUDIO (LIPSTICK AR) ==================== -->
                <section id="tab-beauty" class="p-4 space-y-4 hidden animate-fade-in">
                    
                    <div class="text-center pt-1">
                        <h2 class="text-base font-extrabold text-slate-900">AR Lip Studio</h2>
                        <p class="text-[11px] text-slate-500">จำลองสีลิปสติกเรียลไทม์ตามระดับโทนผิว Light Summer</p>
                    </div>

                    <!-- Face Model Canvas -->
                    <div class="aurora-glass rounded-[28px] p-4 flex flex-col items-center justify-center relative shadow-lg">
                        
                        <div class="relative w-full aspect-square max-w-[220px] flex items-center justify-center">
                            <!-- SVG Stylized Avatar View -->
                            <svg class="w-full h-full" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <!-- Face Contour -->
                                <path d="M100 30 C145 30 160 70 160 110 C160 150 135 180 100 180 C65 180 40 150 40 110 C40 70 55 30 100 30 Z" fill="#FCEBE6"/>
                                <!-- Eyes -->
                                <ellipse cx="75" cy="95" rx="10" ry="6" fill="#332222"/>
                                <ellipse cx="125" cy="95" rx="10" ry="6" fill="#332222"/>
                                <circle cx="77" cy="93" r="2.5" fill="#FFFFFF"/>
                                <circle cx="127" cy="93" r="2.5" fill="#FFFFFF"/>
                                <!-- Eyebrows -->
                                <path d="M62 82 Q75 78 88 83" stroke="#553322" stroke-width="2.5" stroke-linecap="round"/>
                                <path d="M112 83 Q125 78 138 82" stroke="#553322" stroke-width="2.5" stroke-linecap="round"/>
                                <!-- Nose -->
                                <path d="M100 98 L100 120 L104 122" stroke="#E2B1A3" stroke-width="2" stroke-linecap="round"/>
                                
                                <!-- DYNAMIC CHEEK BLUSH -->
                                <ellipse id="ar-blush-left" cx="65" cy="122" rx="16" ry="10" fill="#EC4899" opacity="0.35" class="transition-all duration-300 blur-sm"/>
                                <ellipse id="ar-blush-right" cx="135" cy="122" rx="16" ry="10" fill="#EC4899" opacity="0.35" class="transition-all duration-300 blur-sm"/>

                                <!-- DYNAMIC LIPS AR LAYER -->
                                <path id="ar-upper-lip" d="M80 142 Q90 137 100 140 Q110 137 120 142 Q110 148 100 147 Q90 148 80 142 Z" fill="#E11D48" opacity="0.85" class="transition-all duration-300"/>
                                <path id="ar-lower-lip" d="M80 142 Q100 158 120 142 Q110 152 100 152 Q90 152 80 142 Z" fill="#BE123C" opacity="0.88" class="transition-all duration-300"/>
                            </svg>
                        </div>

                        <!-- Before / After Touch Button -->
                        <button onmousedown="toggleARBefore(true)" onmouseup="toggleARBefore(false)" class="absolute bottom-3 right-3 white-pill px-3 py-1 text-[10px] font-extrabold text-purple-800 shadow-xs active:scale-95">
                            <i class="fa-solid fa-eye mr-1"></i> กดค้างดู Before
                        </button>
                    </div>

                    <!-- Glossy Color Swatch Pills Selector -->
                    <div class="liquid-glass p-3.5 rounded-2xl space-y-3">
                        <div class="flex items-center justify-between">
                            <span class="text-xs font-bold text-slate-800">เลือกเฉดสีลิปสติก (Lipstick Shade)</span>
                            <span id="shade-title" class="text-xs font-bold text-pink-600">#01 Rose Pink Velvet</span>
                        </div>

                        <!-- Glossy Swatch Pill Dots -->
                        <div class="flex items-center justify-between gap-1">
                            <button onclick="setLipShade('#E11D48', '#BE123C', '#01 Rose Pink Velvet')" class="w-8 h-8 rounded-full bg-[#E11D48] border-2 border-purple-500 shadow-xs transform scale-110"></button>
                            <button onclick="setLipShade('#D946EF', '#C026D3', '#02 Soft Berry Gloss')" class="w-8 h-8 rounded-full bg-[#D946EF] border-2 border-white shadow-xs"></button>
                            <button onclick="setLipShade('#F43F5E', '#E11D48', '#03 Blossom Pink')" class="w-8 h-8 rounded-full bg-[#F43F5E] border-2 border-white shadow-xs"></button>
                            <button onclick="setLipShade('#9F1239', '#881337', '#04 Deep Plum')" class="w-8 h-8 rounded-full bg-[#9F1239] border-2 border-white shadow-xs"></button>
                            <button onclick="setLipShade('#FB923C', '#EA580C', '#05 Nude Peach')" class="w-8 h-8 rounded-full bg-[#FB923C] border-2 border-white shadow-xs"></button>
                        </div>

                        <!-- Texture Finish Selector Pills -->
                        <div class="pt-1">
                            <span class="text-[10px] font-bold text-slate-500 mb-1.5 block">เลือกลักษณะเนื้อสัมผัส (Texture):</span>
                            <div class="grid grid-cols-3 gap-2">
                                <button onclick="setLipTexture('Velvet', 0.85)" class="white-pill py-1.5 text-[10px] font-bold text-slate-700 active:scale-95">Velvet Satin</button>
                                <button onclick="setLipTexture('Matte', 1.0)" class="white-pill py-1.5 text-[10px] font-bold text-slate-700 active:scale-95">Soft Matte</button>
                                <button onclick="setLipTexture('Gloss', 0.65)" class="white-pill py-1.5 text-[10px] font-bold text-slate-700 active:scale-95">Dewy Gloss</button>
                            </div>
                        </div>
                    </div>

                    <!-- Save Shade Product Button -->
                    <button onclick="showToast('บันทึกเฉดสีนี้ลงใน Wishlist เรียบร้อยแล้ว 💄')" class="w-full py-3 pill-cta-teal text-white text-xs font-extrabold flex items-center justify-center gap-2 active:scale-95">
                        <i class="fa-solid fa-heart"></i>
                        <span>บันทึกเฉดสีนี้ลงในโปรไฟล์</span>
                    </button>

                </section>

            </div>

            <!-- FLOATING LIQUID GLASS BOTTOM NAVIGATION BAR -->
            <div class="absolute bottom-5 inset-x-4 h-16 liquid-glass rounded-full shadow-2xl flex items-center justify-around px-2 z-40">
                
                <!-- Tab Item 1: Home -->
                <button id="nav-tab-home" onclick="navigateTo('tab-home')" class="flex flex-col items-center justify-center w-14 h-12 rounded-full text-purple-600 transition-all duration-200">
                    <i class="fa-solid fa-house-chimney text-base"></i>
                    <span class="text-[9px] font-bold mt-0.5">หน้าแรก</span>
                </button>

                <!-- Tab Item 2: Scanner -->
                <button id="nav-tab-scanner" onclick="navigateTo('tab-scanner')" class="flex flex-col items-center justify-center w-14 h-12 rounded-full text-slate-400 hover:text-slate-600 transition-all duration-200">
                    <i class="fa-solid fa-camera-retro text-base"></i>
                    <span class="text-[9px] font-semibold mt-0.5">สแกนสี</span>
                </button>

                <!-- Tab Item 3: Wardrobe -->
                <button id="nav-tab-wardrobe" onclick="navigateTo('tab-wardrobe')" class="flex flex-col items-center justify-center w-14 h-12 rounded-full text-slate-400 hover:text-slate-600 transition-all duration-200">
                    <i class="fa-solid fa-shirt text-base"></i>
                    <span class="text-[9px] font-semibold mt-0.5">แมตช์ชุด</span>
                </button>

                <!-- Tab Item 4: Beauty -->
                <button id="nav-tab-beauty" onclick="navigateTo('tab-beauty')" class="flex flex-col items-center justify-center w-14 h-12 rounded-full text-slate-400 hover:text-slate-600 transition-all duration-200">
                    <i class="fa-solid fa-wand-magic-sparkles text-base"></i>
                    <span class="text-[9px] font-semibold mt-0.5">บิวตี้ AR</span>
                </button>

            </div>

            <!-- iOS Bottom Home Indicator Bar -->
            <div class="absolute bottom-1 left-1/2 -translate-x-1/2 w-32 h-1 bg-slate-900/40 rounded-full z-50 pointer-events-none"></div>

        </div>
    </div>

    <!-- Toast Notification Message -->
    <div id="toast-msg" class="fixed bottom-6 white-pill px-4 py-2 text-xs font-bold text-slate-800 shadow-2xl opacity-0 transition-opacity duration-300 pointer-events-none z-50 flex items-center gap-2">
        <i class="fa-solid fa-circle-check text-emerald-500"></i>
        <span id="toast-text">คัดลอกข้อมูลสำเร็จแล้ว</span>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // Update iOS Clock
        function updateClock() {
            const now = new Date();
            const hours = String(now.getHours()).padStart(2, '0');
            const minutes = String(now.getMinutes()).padStart(2, '0');
            document.getElementById('ios-time').textContent = `${hours}:${minutes}`;
        }
        setInterval(updateClock, 1000);
        updateClock();

        // SPA Navigation State Switcher
        function navigateTo(tabId) {
            const tabs = ['tab-home', 'tab-scanner', 'tab-wardrobe', 'tab-beauty'];
            
            // Hide all tabs
            tabs.forEach(id => {
                const el = document.getElementById(id);
                if (el) el.classList.add('hidden');
            });

            // Show active tab
            const target = document.getElementById(tabId);
            if (target) {
                target.classList.remove('hidden');
            }

            // Update Tab Bar Active Button
            tabs.forEach(id => {
                const navBtn = document.getElementById('nav-' + id);
                if (navBtn) {
                    if (id === tabId) {
                        navBtn.className = "flex flex-col items-center justify-center w-14 h-12 rounded-full text-purple-600 font-bold transition-all duration-200 scale-105";
                    } else {
                        navBtn.className = "flex flex-col items-center justify-center w-14 h-12 rounded-full text-slate-400 hover:text-slate-600 font-semibold transition-all duration-200";
                    }
                }
            });

            // Scroll top
            document.getElementById('app-viewport').scrollTop = 0;
        }

        // ================= TAB 2 SCANNER LOGIC =================
        const presetPhotos = {
            cool: 'https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=600&q=80',
            warm: 'https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=600&q=80',
            spring: 'https://images.unsplash.com/photo-1524504388940-b1c1722653e1?auto=format&fit=crop&w=600&q=80'
        };

        function changeScanPreset(type) {
            const img = document.getElementById('scanner-preview-img');
            if (presetPhotos[type]) {
                img.src = presetPhotos[type];
                showToast("สลับภาพตัวอย่าง " + type.toUpperCase());
            }
        }

        function runAIScan() {
            const beam = document.getElementById('scan-beam');
            const btn = document.getElementById('btn-start-scan');
            
            beam.classList.remove('hidden');
            btn.disabled = true;
            btn.innerHTML = `<i class="fa-solid fa-spinner fa-spin"></i><span>กำลังประมวลผล Liquid Glass AI...</span>`;

            setTimeout(() => {
                beam.classList.add('hidden');
                btn.disabled = false;
                btn.innerHTML = `<i class="fa-solid fa-sparkles"></i><span>เริ่มวิเคราะห์สีผิว (ANALYZE NOW)</span>`;
                
                showToast("วิเคราะห์ Personal Color สำเร็จ!");
            }, 2000);
        }

        // ================= TAB 3 WARDROBE LOGIC =================
        function setGarmentColor(type, hexColor, colorName, scoreValue) {
            if (type === 'top') {
                document.getElementById('garment-top').style.backgroundColor = hexColor;
                document.getElementById('top-color-label').textContent = colorName;
            } else if (type === 'bottom') {
                document.getElementById('garment-bottom').style.backgroundColor = hexColor;
                document.getElementById('bottom-color-label').textContent = colorName;
            }

            // Update Match Percentage and Animated Circle Ring
            const scoreNum = document.getElementById('match-score-num');
            const adviceTitle = document.getElementById('match-advice-title');
            const ring = document.getElementById('match-ring');

            scoreNum.textContent = scoreValue + "%";

            // SVG Circumference = 2 * PI * 20 ≈ 125.6
            const offset = 125.6 - (125.6 * scoreValue) / 100;
            ring.style.strokeDashoffset = offset;

            if (scoreValue >= 90) {
                adviceTitle.textContent = "Perfect Harmony 🌸";
                scoreNum.className = "absolute text-xs font-extrabold text-purple-700";
                ring.setAttribute('stroke', '#9B62FF');
            } else if (scoreValue >= 70) {
                adviceTitle.textContent = "Moderate Match ⚡";
                scoreNum.className = "absolute text-xs font-extrabold text-amber-600";
                ring.setAttribute('stroke', '#F59E0B');
            } else {
                adviceTitle.textContent = "Clashing Tones ⚠️";
                scoreNum.className = "absolute text-xs font-extrabold text-rose-600";
                ring.setAttribute('stroke', '#E11D48');
            }
        }

        // ================= TAB 4 BEAUTY STUDIO LOGIC =================
        function setLipShade(mainHex, darkHex, titleName) {
            document.getElementById('ar-upper-lip').setAttribute('fill', mainHex);
            document.getElementById('ar-lower-lip').setAttribute('fill', darkHex);
            document.getElementById('shade-title').textContent = titleName;
            showToast("สลับเป็นสี " + titleName);
        }

        function setLipTexture(textureName, opacity) {
            document.getElementById('ar-upper-lip').setAttribute('opacity', opacity);
            document.getElementById('ar-lower-lip').setAttribute('opacity', opacity);
            showToast("สลับฟินิชเนื้อลิปเป็น " + textureName);
        }

        function toggleARBefore(isBefore) {
            if (isBefore) {
                document.getElementById('ar-upper-lip').setAttribute('opacity', '0.1');
                document.getElementById('ar-lower-lip').setAttribute('opacity', '0.1');
            } else {
                document.getElementById('ar-upper-lip').setAttribute('opacity', '0.85');
                document.getElementById('ar-lower-lip').setAttribute('opacity', '0.85');
            }
        }

        // Toast Notification Function
        function showToast(message) {
            const toast = document.getElementById('toast-msg');
            const text = document.getElementById('toast-text');
            text.textContent = message;
            
            toast.classList.remove('opacity-0');
            toast.classList.add('opacity-100');

            setTimeout(() => {
                toast.classList.remove('opacity-100');
                toast.classList.add('opacity-0');
            }, 2500);
        }
    </script>
</body>
</html>
