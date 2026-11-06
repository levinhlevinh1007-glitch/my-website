<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Business Analytics - Phân Tích Kinh Doanh</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Chart.js CDN -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
</head>
<body class="bg-slate-900 text-slate-100 font-sans min-h-screen">

    <div class="flex h-screen overflow-hidden">
        <!-- Sidebar -->
        <aside class="w-64 bg-slate-800 border-r border-slate-700 p-6 flex flex-col justify-between hidden md:flex">
            <div>
                <div class="flex items-center gap-3 mb-8">
                    <div class="p-2 bg-indigo-600 rounded-lg">
                        <i data-lucide="bot" class="w-6 h-6 text-white"></i>
                    </div>
                    <h1 class="text-xl font-bold text-white tracking-wide">BizAI Insight</h1>
                </div>
                
                <nav class="space-y-2">
                    <a href="#" class="flex items-center gap-3 px-4 py-3 bg-indigo-600 text-white rounded-xl font-medium">
                        <i data-lucide="layout-dashboard" class="w-5 h-5"></i> Tổng quan
                    </a>
                    <a href="#" class="flex items-center gap-3 px-4 py-3 text-slate-400 hover:bg-slate-700/50 hover:text-slate-200 rounded-xl transition">
                        <i data-lucide="trending-up" class="w-5 h-5"></i> Doanh thu & Chi phí
                    </a>
                    <a href="#" class="flex items-center gap-3 px-4 py-3 text-slate-400 hover:bg-slate-700/50 hover:text-slate-200 rounded-xl transition">
                        <i data-lucide="users" class="w-5 h-5"></i> Khách hàng
                    </a>
                    <a href="#" class="flex items-center gap-3 px-4 py-3 text-slate-400 hover:bg-slate-700/50 hover:text-slate-200 rounded-xl transition">
                        <i data-lucide="sparkles" class="w-5 h-5"></i> AI Forecasting
                    </a>
                </nav>
            </div>

            <div class="p-4 bg-slate-700/40 rounded-xl border border-slate-700">
                <p class="text-xs text-slate-400">Trạng thái AI</p>
                <div class="flex items-center gap-2 mt-1 text-emerald-400 text-sm font-medium">
                    <span class="w-2 h-2 bg-emerald-400 rounded-full animate-pulse"></span> Sẵn sàng phân tích
                </div>
            </div>
        </aside>

        <!-- Main Content -->
        <main class="flex-1 overflow-y-auto p-6 lg:p-10">
            <!-- Header -->
            <header class="flex flex-col md:flex-row md:items-center justify-between gap-4 mb-8">
                <div>
                    <h2 class="text-2xl font-bold text-white">Báo Cáo Phân Tích Kinh Doanh</h2>
                    <p class="text-slate-400 text-sm">Theo dõi chỉ số hiệu suất & nhận đề xuất từ AI thông minh</p>
                </div>
                <div class="flex gap-3">
                    <button onclick="runAIAnalysis()" class="flex items-center gap-2 px-5 py-2.5 bg-indigo-600 hover:bg-indigo-500 text-white rounded-xl font-medium transition shadow-lg shadow-indigo-600/30">
                        <i data-lucide="sparkles" class="w-4 h-4"></i> Phân tích ngay bằng AI
                    </button>
                </div>
            </header>

            <!-- Key Metrics Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 mb-8">
                <div class="bg-slate-800 p-6 rounded-2xl border border-slate-700">
                    <div class="flex items-center justify-between text-slate-400 mb-2">
                        <span class="text-sm">Tổng Doanh Thu</span>
                        <i data-lucide="dollar-sign" class="w-5 h-5 text-indigo-400"></i>
                    </div>
                    <div class="text-2xl font-bold text-white">1,245,000,000 ₫</div>
                    <div class="text-xs text-emerald-400 font-medium mt-2 flex items-center gap-1">
                        <i data-lucide="arrow-up-right" class="w-4 h-4"></i> +12.5% so với tháng trước
                    </div>
                </div>

                <div class="bg-slate-800 p-6 rounded-2xl border border-slate-700">
                    <div class="flex items-center justify-between text-slate-400 mb-2">
                        <span class="text-sm">Chi Phí Vận Hành</span>
                        <i data-lucide="credit-card" class="w-5 h-5 text-amber-400"></i>
                    </div>
                    <div class="text-2xl font-bold text-white">450,000,000 ₫</div>
                    <div class="text-xs text-rose-400 font-medium mt-2 flex items-center gap-1">
                        <i data-lucide="arrow-up-right" class="w-4 h-4"></i> +4.2% so với tháng trước
                    </div>
                </div>

                <div class="bg-slate-800 p-6 rounded-2xl border border-slate-700">
                    <div class="flex items-center justify-between text-slate-400 mb-2">
                        <span class="text-sm">Lợi Nhuận Ròng</span>
                        <i data-lucide="pie-chart" class="w-5 h-5 text-emerald-400"></i>
                    </div>
                    <div class="text-2xl font-bold text-white">795,000,000 ₫</div>
                    <div class="text-xs text-emerald-400 font-medium mt-2 flex items-center gap-1">
                        <i data-lucide="arrow-up-right" class="w-4 h-4"></i> +18.1% so với tháng trước
                    </div>
                </div>

                <div class="bg-slate-800 p-6 rounded-2xl border border-slate-700">
                    <div class="flex items-center justify-between text-slate-400 mb-2">
                        <span class="text-sm">Khách Hàng Mới</span>
                        <i data-lucide="user-plus" class="w-5 h-5 text-blue-400"></i>
                    </div>
                    <div class="text-2xl font-bold text-white">1,280</div>
                    <div class="text-xs text-emerald-400 font-medium mt-2 flex items-center gap-1">
                        <i data-lucide="arrow-up-right" class="w-4 h-4"></i> +8.4% so với tháng trước
                    </div>
                </div>
            </div>

            <!-- Chart & AI Section -->
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-8">
                <!-- Revenue Chart -->
                <div class="lg:col-span-2 bg-slate-800 p-6 rounded-2xl border border-slate-700">
                    <h3 class="text-lg font-semibold text-white mb-4">Xu hướng Tài chính 6 Tháng qua</h3>
                    <div class="h-72">
                        <canvas id="businessChart"></canvas>
                    </div>
                </div>

                <!-- AI Insights Panel -->
                <div class="bg-slate-800 p-6 rounded-2xl border border-slate-700 flex flex-col justify-between">
                    <div>
                        <div class="flex items-center gap-2 mb-4 text-indigo-400 font-semibold">
                            <i data-lucide="bot" class="w-5 h-5"></i>
                            <h3>Khuyến Nghị Từ AI</h3>
                        </div>
                        <div id="aiInsightContainer" class="space-y-4 text-sm text-slate-300">
                            <p class="text-slate-400 italic">Nhấn nút "Phân tích ngay bằng AI" để hệ thống tổng hợp báo cáo chiến lược cho bạn...</p>
                        </div>
                    </div>
                    
                    <div class="mt-6 pt-4 border-t border-slate-700 flex items-center justify-between text-xs text-slate-400">
                        <span>Được tối ưu bởi AI Engine</span>
                        <span class="text-indigo-400 cursor-pointer hover:underline" onclick="runAIAnalysis()">Tải lại phân tích</span>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <script>
        // Khởi tạo biểu tượng Lucide
        lucide.createIcons();

        // Data mẫu cho biểu đồ
        const financialData = {
            labels: ['Tháng 6', 'Tháng 7', 'Tháng 8', 'Tháng 9', 'Tháng 10', 'Tháng 11'],
            revenue: [850, 920, 1050, 980, 1150, 1245],
            expenses: [400, 410, 430, 420, 440, 450],
            profit: [450, 510, 620, 560, 710, 795]
        };

        // Vẽ biểu đồ Chart.js
        const ctx = document.getElementById('businessChart').getContext('2d');
        new Chart(ctx, {
            type: 'line',
            data: {
                labels: financialData.labels,
                datasets: [
                    {
                        label: 'Doanh thu (Triệu ₫)',
                        data: financialData.revenue,
                        borderColor: '#6366f1',
                        backgroundColor: 'rgba(99, 102, 241, 0.1)',
                        tension: 0.4,
                        fill: true
                    },
                    {
                        label: 'Chi phí (Triệu ₫)',
                        data: financialData.expenses,
                        borderColor: '#f59e0b',
                        tension: 0.4
                    },
                    {
                        label: 'Lợi nhuận (Triệu ₫)',
                        data: financialData.profit,
                        borderColor: '#10b981',
                        tension: 0.4
                    }
                ]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: {
                    legend: { labels: { color: '#94a3b8' } }
                },
                scales: {
                    x: { ticks: { color: '#94a3b8' }, grid: { color: '#334155' } },
                    y: { ticks: { color: '#94a3b8' }, grid: { color: '#334155' } }
                }
            }
        });

        // Hàm giả lập phân tích AI
        function runAIAnalysis() {
            const container = document.getElementById('aiInsightContainer');
            
            // Đặt trạng thái đang tải
            container.innerHTML = `
                <div class="flex items-center gap-3 text-indigo-400 animate-pulse py-4">
                    <i data-lucide="loader" class="w-5 h-5 animate-spin"></i>
                    <span>AI đang phân tích biểu đồ và các chỉ số...</span>
                </div>
            `;
            lucide.createIcons();

            // Giả lập delay xử lý AI
            setTimeout(() => {
                container.innerHTML = `
                    <div class="p-3 bg-indigo-950/40 border border-indigo-800/50 rounded-xl space-y-2">
                        <div class="font-semibold text-indigo-300 flex items-center gap-1.5">
                            <i data-lucide="trending-up" class="w-4 h-4"></i> Tăng trưởng ấn tượng
                        </div>
                        <p class="text-xs text-slate-300">Doanh thu Tháng 11 đạt đỉnh 1.245 tỷ ₫ (+12.5%). Tỷ lệ biên lợi nhuận ròng tăng vượt mức 63%.</p>
                    </div>

                    <div class="p-3 bg-amber-950/40 border border-amber-800/50 rounded-xl space-y-2">
                        <div class="font-semibold text-amber-300 flex items-center gap-1.5">
                            <i data-lucide="alert-triangle" class="w-4 h-4"></i> Cảnh báo Chi phí
                        </div>
                        <p class="text-xs text-slate-300">Chi phí vận hành tăng nhẹ 4.2%. Cần tối ưu lại ngân sách Marketing vào các kênh có ROI cao hơn.</p>
                    </div>

                    <div class="p-3 bg-emerald-950/40 border border-emerald-800/50 rounded-xl space-y-2">
                        <div class="font-semibold text-emerald-300 flex items-center gap-1.5">
                            <i data-lucide="check-circle" class="w-4 h-4"></i> Khuyến nghị Chiến lược
                        </div>
                        <p class="text-xs text-slate-300">Tăng 15% ngân sách giữ chân khách hàng hiện tại để tối ưu chỉ số LTV (Lifetime Value).</p>
                    </div>
                `;
                lucide.createIcons();
            }, 1200);
        }
    </script>
</body>
</html>
