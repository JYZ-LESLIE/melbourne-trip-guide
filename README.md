<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2026 墨尔本商务与团建手册 (Final v18)</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#1E40AF', // 深蓝
                        secondary: '#3B82F6', // 亮蓝
                        accent: '#F59E0B', // 琥珀
                        neutral: '#F8FAFC',
                        dark: '#1E293B',
                    },
                    fontFamily: { sans: ['Inter', 'sans-serif'] }
                }
            }
        }
    </script>
    <style>
        /* Card Styles */
        .card { background: white; border-radius: 12px; padding: 20px; border: 1px solid #e2e8f0; box-shadow: 0 1px 3px rgba(0,0,0,0.02); position: relative; z-index: 10; transition: transform 0.2s; }
        .card:hover { transform: translateY(-2px); box-shadow: 0 10px 15px -3px rgba(0,0,0,0.05); border-color: #93c5fd; }
        
        /* Timeline Flow */
        .flow-container { position: relative; padding-left: 24px; }
        .flow-line { position: absolute; left: 11px; top: 20px; bottom: -20px; width: 2px; background: #e2e8f0; z-index: 0; border-left: 2px dashed #cbd5e1; }
        .flow-time { 
            display: inline-flex; align-items: center; gap: 6px;
            margin: 16px 0 16px 12px; font-size: 0.75rem; color: #64748b; 
            background: #f1f5f9; padding: 4px 10px; border-radius: 20px; font-weight: 600;
            border: 1px solid #e2e8f0; position: relative; z-index: 1;
        }

        /* Typography & Components */
        .day-badge { background: #1E40AF; color: white; font-weight: 800; font-size: 0.85rem; padding: 4px 10px; border-radius: 6px; box-shadow: 0 2px 4px rgba(30, 64, 175, 0.2); }
        .section-header { display: flex; align-items: center; gap: 12px; margin: 40px 0 20px 0; padding-bottom: 12px; border-bottom: 2px solid #e2e8f0; }
        
        .selling-point { 
            background: #fffbeb; border-left: 3px solid #F59E0B; color: #92400e; 
            font-style: italic; font-size: 0.85rem; padding: 10px 14px; margin-bottom: 12px; border-radius: 0 6px 6px 0;
        }
        
        .badge-cost { background: #ecfdf5; color: #047857; border: 1px solid #6ee7b7; font-family: monospace; padding: 2px 8px; border-radius: 4px; font-size: 0.75rem; font-weight: 600; }
        .badge-time { background: #eff6ff; color: #1e40af; padding: 2px 8px; border-radius: 4px; font-size: 0.75rem; font-weight: 600; }
        
        .btn-link { 
            font-size: 0.75rem; color: #334155; text-decoration: none; font-weight: 600;
            background: #f8fafc; padding: 6px 12px; border-radius: 6px; border: 1px solid #cbd5e1;
            display: inline-flex; align-items: center; gap: 4px; transition: all 0.2s;
        }
        .btn-link:hover { background: #eff6ff; border-color: #3b82f6; color: #1d4ed8; }

        /* Cost Toggle */
        .hidden-cost .badge-cost { display: none !important; }

        /* --- DRIVING MODAL (V13 Feature Restored) --- */
        .modal-overlay { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.7); z-index: 100; backdrop-filter: blur(4px); }
        .drive-modal { 
            display: none; position: fixed; top: 50%; left: 50%; transform: translate(-50%, -50%); 
            width: 90%; max-width: 600px; max-height: 85vh; overflow-y: auto; 
            background: white; border-radius: 16px; z-index: 101; box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
        }
        .drive-header { position: sticky; top: 0; background: #1E40AF; color: white; padding: 16px 20px; display: flex; justify-content: space-between; align-items: center; z-index: 10; }
        
        /* CSS Traffic Signs (No Images) */
        .sign-hook { 
            border: 3px solid black; border-radius: 4px; width: 60px; height: 70px; 
            display: flex; flex-direction: column; align-items: center; justify-content: center; 
            background: white; font-weight: 900; font-size: 9px; line-height: 1.2; text-align: center; font-family: sans-serif;
            box-shadow: 2px 2px 0px rgba(0,0,0,0.1);
        }
        .sign-p { 
            border: 2px solid #15803d; border-radius: 4px; width: 45px; height: 60px; 
            background: white; display: flex; flex-direction: column; overflow: hidden;
        }
        .sign-p-top { height: 60%; display: flex; align-items: center; justify-content: center; font-weight: 900; color: #15803d; font-size: 20px; }
        .sign-p-bot { height: 40%; background: #15803d; color: white; font-size: 7px; display: flex; align-items: center; justify-content: center; text-align: center; line-height: 1.1; font-weight: bold; }
    </style>
</head>
<body class="bg-neutral pb-12" id="main-body">

    <nav class="sticky top-0 z-50 bg-primary text-white shadow-lg">
        <div class="max-w-4xl mx-auto px-4 py-3 flex justify-between items-center">
            <div>
                <h1 class="font-bold text-base tracking-wide flex items-center gap-2">
                    <i class="fa fa-map-o"></i> MELBOURNE OPS
                </h1>
                <div class="flex gap-3 text-[10px] text-blue-200 mt-0.5">
                    <span>8人团队</span>
                    <span>1.24 - 2.04</span>
                </div>
            </div>
            <div class="flex gap-2">
                <button onclick="openDriveModal()" class="bg-accent hover:bg-yellow-500 text-white text-xs font-bold px-3 py-1.5 rounded transition shadow-sm flex items-center gap-1 animate-pulse">
                    <i class="fa fa-car"></i> 驾驶速成
                </button>
                <button onclick="toggleCosts()" class="text-xs bg-blue-900/50 border border-blue-400/30 px-3 py-1.5 rounded hover:bg-blue-800 transition flex items-center gap-1">
                    <i class="fa fa-eye" id="eye-icon"></i> <span id="toggle-text">隐藏费用</span>
                </button>
            </div>
        </div>
    </nav>

    <main class="max-w-4xl mx-auto px-4 py-6 fade-in">

        <!-- 仪表盘 -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-8">
            <div class="card border-l-4 border-l-secondary">
                <h3 class="font-bold text-dark text-sm mb-2 flex items-center"><i class="fa fa-thermometer-half mr-2 text-secondary"></i>天气 & 穿衣</h3>
                <ul class="list-disc list-inside text-xs text-gray-600 space-y-1">
                    <li><strong>气温:</strong> 15-35°C (夏季温差极大)。</li>
                    <li><strong>穿衣:</strong> T恤 + <strong>薄卫衣/防风衣</strong> (早晚必穿)。</li>
                    <li><strong>防晒:</strong> 紫外线极强！务必携带墨镜、帽子。</li>
                </ul>
            </div>
            <div class="card border-l-4 border-l-accent">
                <h3 class="font-bold text-dark text-sm mb-2 flex items-center"><i class="fa fa-plug mr-2 text-accent"></i>电源 & 支付</h3>
                <ul class="list-disc list-inside text-xs text-gray-600 space-y-1">
                    <li><strong>插座:</strong> 澳标 <strong>八字形三扁插头</strong> (Type I)。</li>
                    <li><strong>支付:</strong> 99%支持刷卡。备少量现金 ($100) 即可。</li>
                </ul>
            </div>
        </div>

        <!-- 1.31 SAT -->
        <div class="section-header">
            <span class="day-badge">1.31 SAT</span>
            <span class="font-bold text-lg text-dark">大洋路精华自驾 (无十二门徒)</span>
        </div>
        
        <div class="flow-container">
            <div class="flow-line"></div>

            <div class="flow-time"><i class="fa fa-car"></i> 09:00 出发 -> 1h 车程</div>
            
            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">Geelong Waterfront (吉朗海滨)</h3>
                    <span class="badge badge-time">停留 1h</span>
                </div>
                <div class="selling-point">“在维州第二大城的海滨，寻觅百个形态各异的彩绘木偶人，是团队合影的最佳背景。”</div>
                <span class="badge badge-cost">💰 免费</span>
                <div class="mt-4 flex gap-2 flex-wrap border-t border-gray-100 pt-3">
                    <a href="https://www.google.com/maps/search/Geelong+Waterfront" target="_blank" class="btn-link"><i class="fa fa-location-arrow"></i> 导航</a>
                    <a href="https://m.mafengwo.cn/poi/6561571.html" target="_blank" class="btn-link"><i class="fa fa-file-text-o"></i> 攻略</a>
                </div>
            </div>

            <div class="flow-time"><i class="fa fa-car"></i> 1h 车程 (B100海岸公路)</div>

            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">Lorne Hotel Pub (午餐)</h3>
                    <span class="badge badge-time">停留 1.5h</span>
                </div>
                <div class="selling-point">“坐在悬崖之上的百年酒馆，点一份澳洲最地道的炸鱼薯条，眼前就是无尽的南太平洋。”</div>
                <span class="badge badge-cost">💰 人均约 $35 AUD</span>
                <div class="mt-4 border-t border-gray-100 pt-3">
                    <a href="https://www.tripadvisor.com/Restaurant_Review-g552200-d1753982-Reviews-Lorne_Hotel_Bistro-Lorne_Victoria.html" target="_blank" class="btn-link"><i class="fa fa-star-o"></i> 真实评价</a>
                </div>
            </div>

            <div class="flow-time"><i class="fa fa-car"></i> 10min 上山路</div>

            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">Teddy's Lookout (泰迪观景台)</h3>
                    <span class="badge badge-time">停留 0.5h</span>
                </div>
                <div class="selling-point">“无需无人机，也能拥有上帝视角。俯瞰大洋路最美发卡弯，这是无数明信片的诞生地。”</div>
                <span class="badge badge-cost">💰 免费</span>
                <div class="mt-4 border-t border-gray-100 pt-3">
                    <a href="https://www.google.com/maps/search/Teddy's+Lookout" target="_blank" class="btn-link"><i class="fa fa-location-arrow"></i> 导航</a>
                </div>
            </div>
        </div>

        <!-- 2.01 SUN -->
        <div class="section-header">
            <span class="day-badge">2.01 SUN</span>
            <span class="font-bold text-lg text-dark">澳网决赛日 & 动物园</span>
        </div>

        <div class="flow-container">
            <div class="flow-line"></div>
            
            <div class="flow-time"><i class="fa fa-car"></i> 08:30 出发 -> 50min 车程</div>

            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">Healesville Sanctuary</h3>
                    <span class="badge badge-time">09:30 - 12:30</span>
                </div>
                <div class="selling-point">“森林深处的本土动物避难所。必看：鸭嘴兽馆、考拉近距离接触、12:00猛禽秀。”</div>
                <span class="badge badge-cost">💰 门票约 $46 AUD</span>
                <div class="mt-4 border-t border-gray-100 pt-3">
                    <a href="https://www.zoo.org.au/healesville" target="_blank" class="btn-link"><i class="fa fa-ticket"></i> 官网购票</a>
                </div>
            </div>

            <div class="flow-time"><i class="fa fa-car"></i> 1h 车程 (回市区)</div>

            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">Melbourne Park (Ground Pass)</h3>
                    <span class="badge badge-time">15:00 至晚间</span>
                </div>
                <div class="selling-point">“置身蓝色硬地场外的草坪派对，与数万名球迷共同见证大满贯冠军时刻的狂热氛围。”</div>
                <span class="badge badge-cost">💰 外场票约 $29 AUD</span>
                <div class="mt-4 border-t border-gray-100 pt-3">
                    <a href="https://www.ticketmaster.com.au/" target="_blank" class="btn-link"><i class="fa fa-ticket"></i> Ticketmaster</a>
                </div>
            </div>
        </div>

        <!-- 2.02 MON -->
        <div class="section-header">
            <span class="day-badge">2.02 MON</span>
            <span class="font-bold text-lg text-dark">莫宁顿半岛 (无温泉)</span>
        </div>
        
        <div class="flow-container">
            <div class="flow-line"></div>
            <div class="flow-time"><i class="fa fa-car"></i> 50min 车程</div>

            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">Arthur's Seat Eagle (缆车)</h3>
                    <span class="badge badge-time">停留 1h</span>
                </div>
                <div class="selling-point">“乘坐瑞士制造的缆车，像老鹰一样翱翔在菲利普湾的碧蓝之上，俯瞰整个半岛。”</div>
                <span class="badge badge-cost">💰 往返约 $34 AUD</span>
                <div class="mt-4 border-t border-gray-100 pt-3">
                    <a href="https://aseagle.com.au/" target="_blank" class="btn-link"><i class="fa fa-ticket"></i> 预订</a>
                </div>
            </div>

            <div class="flow-time"><i class="fa fa-car"></i> 20min 车程</div>

            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">Sorrento & Portsea</h3>
                    <span class="badge badge-time">停留 3h</span>
                </div>
                <div class="selling-point">“先在Sorrento吃一块著名的香草蛋糕，再去半岛最尖端(London Bridge)直面南大洋的巨浪。”</div>
                <span class="badge badge-cost">💰 免费 (午餐另计)</span>
                <div class="mt-4 border-t border-gray-100 pt-3">
                    <a href="https://www.google.com/maps/search/London+Bridge+Lookout+Portsea" target="_blank" class="btn-link"><i class="fa fa-location-arrow"></i> 导航伦敦桥</a>
                </div>
            </div>
        </div>

        <!-- 2.03 TUE -->
        <div class="section-header">
            <span class="day-badge">2.03 TUE</span>
            <span class="font-bold text-lg text-dark">维妈市场 & 古老拱廊</span>
        </div>

        <div class="flow-container">
            <div class="flow-line"></div>
            <div class="flow-time"><i class="fa fa-train"></i> 建议火车/Uber出行 (40min)</div>

            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">Queen Victoria Market</h3>
                    <span class="badge badge-time">10:00 - 12:30</span>
                </div>
                <div class="selling-point">“墨尔本的城市厨房。这里是买伴手礼(UGG/蜂蜜/T恤)性价比最高的地方，还能吃到热腾腾的果酱甜甜圈。”</div>
                <span class="badge badge-cost">💰 丰俭由人</span>
                <div class="mt-4 border-t border-gray-100 pt-3">
                    <a href="https://m.mafengwo.cn/poi/6561571.html" target="_blank" class="btn-link"><i class="fa fa-list-alt"></i> 必买攻略</a>
                </div>
            </div>

            <div class="flow-time"><i class="fa fa-male"></i> 步行 15min</div>

            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">Royal & Block Arcade</h3>
                    <span class="badge badge-time">14:00 - 15:30</span>
                </div>
                <div class="selling-point">“穿越回19世纪的流金岁月，在马赛克地砖和玻璃穹顶下漫步，避开语言门槛，纯享视觉之美。”</div>
                <span class="badge badge-cost">💰 免费</span>
            </div>

            <div class="card bg-gray-50 border-gray-200">
                <h3 class="font-bold text-dark mb-1">🍜 18:00 唐人街自由晚餐 (Farewell)</h3>
                <p class="text-xs text-gray-600">告别宴不搞形式主义。在Chinatown自由享用家乡味（推荐食为先/天府），随后去 Chemist Warehouse 补齐清单。</p>
                <span class="badge badge-cost">💰 预估 $50 AUD/人</span>
            </div>
        </div>

        <!-- 2.04 WED -->
        <div class="section-header">
            <span class="day-badge bg-accent">2.04 WED</span>
            <span class="font-bold text-lg text-dark">最后一日 & 回程</span>
        </div>

        <!-- 交通警报 -->
        <div class="card bg-red-50 border-red-200 shadow-none mb-6">
            <h4 class="font-bold mb-2 text-sm text-red-900"><i class="fa fa-exclamation-triangle mr-2"></i>重要：交通与分流安排</h4>
            <ul class="list-disc list-inside text-xs text-red-800 space-y-1">
                <li><strong>07:00</strong> 领队(唯一司机) 需驾车前往机场还车，飞往新西兰。</li>
                <li><strong>08:30</strong> 团队(6人) 退房。此时<strong>无车</strong>。</li>
                <li><strong>行动建议:</strong> 团队需使用 Uber 或 Maxi Taxi (大出租车) 行动。费用已预估在下方。</li>
            </ul>
        </div>

        <div class="flow-container">
            <div class="flow-line"></div>
            <div class="flow-time"><i class="fa fa-taxi"></i> 打车约 25min</div>

            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">Brighton Bathing Boxes</h3>
                    <span class="badge badge-time">09:30 (停留1h)</span>
                </div>
                <div class="selling-point">“82个色彩斑斓的梦，整齐排列在沙滩上。早上去光线最柔和，人也最少。”</div>
                <span class="badge badge-cost">💰 打车费公摊</span>
                <div class="mt-4 border-t border-gray-100 pt-3">
                    <a href="https://www.google.com/maps/search/Brighton+Bathing+Boxes" target="_blank" class="btn-link"><i class="fa fa-location-arrow"></i> 导航</a>
                </div>
            </div>

            <div class="flow-time"><i class="fa fa-taxi"></i> 打车约 15min</div>

            <div class="card">
                <div class="flex justify-between items-start mb-2">
                    <h3 class="font-bold text-lg text-dark">St Kilda & Luna Park</h3>
                    <span class="badge badge-time">11:30 - 14:00</span>
                </div>
                <div class="selling-point">“在月亮公园的巨大笑脸前打卡，漫步百年栈桥，看一眼CBD的远景天际线。”</div>
            </div>

            <div class="card bg-dark text-white border-0 mt-6">
                <h3 class="font-bold text-lg mb-2 flex items-center"><i class="fa fa-plane mr-2 text-accent"></i>17:00 机场集合 & TRS退税</h3>
                <ul class="list-disc list-inside text-xs text-gray-300 space-y-1">
                    <li>提前下载 <strong>TRS APP</strong> 填好发票信息。</li>
                    <li>液体/保健品若需退税，请在<strong>安检外 (Landside) ABF办公室</strong> 先盖章。</li>
                    <li><strong>20:15 CA166 起飞</strong> -> 平安回国。</li>
                </ul>
            </div>
        </div>

    </main>

    <!-- Driving Rules Modal -->
    <div class="modal-overlay" id="modal-overlay" onclick="closeDriveModal()"></div>
    <div class="drive-modal" id="drive-modal">
        <div class="drive-header">
            <h2 class="text-lg font-bold"><i class="fa fa-car mr-2"></i>墨尔本驾驶速成</h2>
            <button onclick="closeDriveModal()" class="text-white hover:text-accent"><i class="fa fa-times"></i></button>
        </div>
        <div class="drive-body">
            <!-- Rule 1 -->
            <div class="bg-red-50 border-l-4 border-red-500 p-4 rounded mb-4">
                <h3 class="font-bold text-red-900 text-sm mb-1">1. 时刻靠左 (KEEP LEFT)</h3>
                <p class="text-xs text-red-800">最高优先级！无论转弯还是直行，心中默念：<strong>“司机永远在马路中线一侧”</strong>。</p>
            </div>
            
            <!-- Rule 2: Hook Turn -->
            <div class="bg-gray-50 border-l-4 border-gray-800 p-4 rounded mb-4 flex gap-4">
                <div class="sign-hook">
                    <div>RIGHT</div><div>TURN</div><div>FROM</div><div>LEFT</div>
                </div>
                <div>
                    <h3 class="font-bold text-dark text-sm mb-1">2. 勾形转弯 (Hook Turn)</h3>
                    <p class="text-xs text-gray-600">CBD特有：想右转？<strong>靠最左车道</strong>，直行到路口中间停下，等横向绿灯亮起再右转。</p>
                </div>
            </div>

            <!-- Rule 3: Parking -->
            <div class="bg-green-50 border-l-4 border-green-600 p-4 rounded mb-4 flex gap-4">
                <div class="sign-p">
                    <div class="sign-p-top">2P</div>
                    <div class="sign-p-bot">Ticket</div>
                </div>
                <div>
                    <h3 class="font-bold text-green-900 text-sm mb-1">3. 停车天书</h3>
                    <p class="text-xs text-green-800"><strong>2P:</strong> 可停2小时。<strong>Ticket:</strong> 需买票。<strong>Clearway:</strong> 禁停(会被拖走)。</p>
                </div>
            </div>

            <button onclick="closeDriveModal()" class="w-full bg-primary text-white py-3 rounded-lg font-bold mt-2 hover:bg-blue-800 transition">我已了解，安全出发</button>
        </div>
    </div>

    <script>
        function toggleCosts() {
            document.body.classList.toggle('hidden-cost');
            const btn = document.getElementById('toggle-text');
            if (document.body.classList.contains('hidden-cost')) {
                btn.innerText = "显示费用";
            } else {
                btn.innerText = "隐藏费用";
            }
        }
        function openDriveModal() {
            document.getElementById('drive-modal').style.display = 'block';
            document.getElementById('modal-overlay').style.display = 'block';
            document.body.style.overflow = 'hidden';
        }
        function closeDriveModal() {
            document.getElementById('drive-modal').style.display = 'none';
            document.getElementById('modal-overlay').style.display = 'none';
            document.body.style.overflow = 'auto';
        }
    </script>
</body>
</html>
