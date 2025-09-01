<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gemini 로또 번호 심층 분석 (1188회차)</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Chosen Palette: Slate & Amber -->
    <!-- Application Structure Plan: A tabbed single-page application is designed for optimal user experience. The default '종합 분석 및 예측' tab immediately presents the most crucial information: the 1188th draw predictions. This dashboard layout prioritizes the primary user goal. Secondary tabs, '통계 데이터 분석' and '분석 모델링', allow users to delve deeper into the statistical evidence and the analytical methodology respectively. This layered information architecture prevents overwhelming the user while providing comprehensive, explorable content, moving from the "what" to the "why" and "how". -->
    <!-- Visualization & Content Choices: Report Info -> Key predictions -> Goal: Inform -> Presentation: Styled HTML "lotto balls" for intuitive recognition. Report Info -> Hot/Cool/Neutral Ratios -> Goal: Show Proportions -> Viz: Chart.js Doughnut Chart for clear part-to-whole comparison. Report Info -> Consecutive Number Frequency -> Goal: Compare Categories -> Viz: Chart.js Bar Chart for effective frequency comparison across groups. Report Info -> Astrological Charts -> Goal: Provide Evidence -> Presentation: Embedded PNG images with explanatory text. This structure uses the best tool for each data type, ensuring clarity and engagement. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@400;500;700&display=swap');
        body { font-family: 'Noto Sans KR', sans-serif; background-color: #f8fafc; }
        .lotto-ball { display: flex; align-items: center; justify-content: center; width: 2.75rem; height: 2.75rem; border-radius: 50%; color: white; font-weight: bold; font-size: 1.125rem; box-shadow: 0 4px 6px rgba(0,0,0,0.1); margin: 0.25rem; }
        .ball-yellow { background: linear-gradient(135deg, #facc15, #eab308); }
        .ball-blue { background: linear-gradient(135deg, #38bdf8, #0ea5e9); }
        .ball-red { background: linear-gradient(135deg, #f87171, #ef4444); }
        .ball-gray { background: linear-gradient(135deg, #9ca3af, #6b7280); }
        .ball-green { background: linear-gradient(135deg, #4ade80, #22c55e); }
        .tab-btn { transition: all 0.3s ease; }
        .tab-btn.active { color: #0f172a; border-color: #f59e0b; background-color: #fef3c7; }
        .tab-btn:not(.active) { color: #475569; border-color: transparent; }
        .chart-container { position: relative; width: 100%; max-width: 500px; margin-left: auto; margin-right: auto; height: 300px; max-height: 350px; }
        @media (min-width: 768px) { .chart-container { height: 350px; } }
    </style>
</head>
<body class="antialiased text-slate-800">

    <div class="container mx-auto p-4 md:p-8">
        
        <header class="text-center mb-8">
            <h1 class="text-3xl md:text-4xl font-bold text-slate-900">Gemini 로또 번호 심층 분석</h1>
            <p class="text-lg text-slate-600 mt-2">1188회차 (2025.09.06 추첨)</p>
        </header>

        <div class="w-full max-w-4xl mx-auto">
            <nav class="flex justify-center border-b border-slate-200 mb-8" id="tab-navigation">
                <button data-tab="dashboard" class="tab-btn active font-semibold py-3 px-6 border-b-2">종합 분석 및 예측</button>
                <button data-tab="stats" class="tab-btn font-semibold py-3 px-6 border-b-2">통계 데이터 분석</button>
                <button data-tab="methodology" class="tab-btn font-semibold py-3 px-6 border-b-2">분석 모델링</button>
            </nav>

            <main id="tab-content">
                <!-- Dashboard Content -->
                <div id="dashboard-content" class="tab-pane space-y-8">
                    <div class="bg-white p-6 rounded-xl shadow-md border border-slate-100">
                        <h2 class="text-2xl font-bold text-slate-900 mb-4">1188회차 최종 번호 제안</h2>
                        <p class="text-slate-600 mb-6">통계적 패턴, LSTM 모델링 특성, 보정된 천궁도 분석을 종합하여 도출된 최종 번호 조합입니다. 각 조합은 데이터 기반 필터링을 거쳐 최적의 균형을 이루도록 구성되었습니다.</p>
                        
                        <div class="space-y-6">
                            <div>
                                <h3 class="font-bold text-lg text-amber-600 mb-3">반자동 필수 입력 3개 번호</h3>
                                <p class="text-slate-500 text-sm mb-3">목성의 행운(7), 태양의 중심 에너지(14), 달의 흐름(28)을 상징하는 핵심 번호입니다.</p>
                                <div class="flex flex-wrap justify-center sm:justify-start">
                                    <div class="lotto-ball ball-red">7</div>
                                    <div class="lotto-ball ball-red">14</div>
                                    <div class="lotto-ball ball-red">28</div>
                                </div>
                            </div>
                            
                            <div>
                                <h3 class="font-bold text-lg text-amber-600 mb-3">TOP 1 조합 (Best Mix)</h3>
                                <p class="text-slate-500 text-sm mb-3">핫/쿨/중립, 홀짝 비율 등 모든 통계적 균형이 가장 이상적인 최우선 추천 조합입니다.</p>
                                <div class="flex flex-wrap justify-center sm:justify-start">
                                    <div class="lotto-ball ball-yellow">7</div>
                                    <div class="lotto-ball ball-blue">14</div>
                                    <div class="lotto-ball ball-blue">19</div>
                                    <div class="lotto-ball ball-green">25</div>
                                    <div class="lotto-ball ball-green">28</div>
                                    <div class="lotto-ball ball-gray">36</div>
                                </div>
                            </div>

                            <div>
                                <h3 class="font-bold text-lg text-amber-600 mb-3">TOP 5 조합 (추가 4개)</h3>
                                <p class="text-slate-500 text-sm mb-3">다양한 통계적 관점을 강화하여 구성된 차선책 조합들입니다.</p>
                                <div class="flex flex-wrap justify-center sm:justify-start -ml-2">
                                    <div class="p-2 w-full sm:w-1/2 lg:w-auto">
                                        <div class="flex"><div class="lotto-ball ball-yellow">4</div><div class="lotto-ball ball-yellow">7</div><div class="lotto-ball ball-blue">14</div><div class="lotto-ball ball-green">28</div><div class="lotto-ball ball-green">30</div><div class="lotto-ball ball-gray">43</div></div>
                                    </div>
                                    <div class="p-2 w-full sm:w-1/2 lg:w-auto">
                                        <div class="flex"><div class="lotto-ball ball-yellow">7</div><div class="lotto-ball ball-blue">12</div><div class="lotto-ball ball-blue">14</div><div class="lotto-ball ball-green">25</div><div class="lotto-ball ball-gray">33</div><div class="lotto-ball ball-gray">40</div></div>
                                    </div>
                                    <div class="p-2 w-full sm:w-1/2 lg:w-auto">
                                        <div class="flex"><div class="lotto-ball ball-yellow">5</div><div class="lotto-ball ball-blue">14</div><div class="lotto-ball ball-green">22</div><div class="lotto-ball ball-green">28</div><div class="lotto-ball ball-green">30</div><div class="lotto-ball ball-gray">39</div></div>
                                    </div>
                                    <div class="p-2 w-full sm:w-1/2 lg:w-auto">
                                        <div class="flex"><div class="lotto-ball ball-yellow">7</div><div class="lotto-ball ball-blue">17</div><div class="lotto-ball ball-blue">19</div><div class="lotto-ball ball-green">28</div><div class="lotto-ball ball-gray">34</div><div class="lotto-ball ball-gray">45</div></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-white p-6 rounded-xl shadow-md border border-slate-100">
                        <h2 class="text-2xl font-bold text-slate-900 mb-4">2025.09.06 천궁도 트랜짓 분석</h2>
                        <div class="md:flex md:space-x-6">
                            <div class="md:w-1/2">
                                <p class="text-slate-600 mb-4">추첨일의 천체 배치는 이번 회차의 에너지 흐름을 암시합니다. 목성과 금성의 조화로운 각도는 긍정적 기운을 나타내며, 태양, 달, 주요 행성들의 위치와 각도를 분석하여 핵심 번호를 추출했습니다.</p>
                                <ul class="list-disc list-inside text-slate-600 space-y-2">
                                    <li><strong class="text-slate-800">행운의 흐름:</strong> 목성(7° 게자리)과 금성(19° 사자자리)의 조화. 1-20번대 번호에 긍정적 에너지.</li>
                                    <li><strong class="text-slate-800">주요 행성 위치:</strong> 태양(14°), 달(28°), 수성/화성(25°), 토성(30°)의 도수를 핵심 번호로 활용.</li>
                                    <li><strong class="text-slate-800">주요 각도(Aspect):</strong> 달과 토성의 긍정적 삼각(120°) 관계에서 12, 24, 36 등 관련 번호 추출.</li>
                                </ul>
                            </div>
                            <div class="md:w-1/2 mt-6 md:mt-0 flex justify-center items-center">
                                <img src="0906.png" alt="2025년 9월 6일 천궁도" class="rounded-lg shadow-lg w-full max-w-xs">
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Stats Content -->
                <div id="stats-content" class="tab-pane hidden space-y-8">
                    <div class="bg-white p-6 rounded-xl shadow-md border border-slate-100">
                        <h2 class="text-2xl font-bold text-slate-900 mb-2">핫/쿨/중립 넘버 분석</h2>
                        <p class="text-slate-600 mb-6">역대 당첨 빈도를 기준으로 번호를 세 그룹으로 분류하고, 당첨 조합에서 이들 그룹의 비율이 어떻게 나타나는지 분석합니다. 특정 그룹에 편중되기보다 균형 잡힌 조합이 더 높은 빈도를 보입니다.</p>
                        
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-8 text-center">
                            <div class="bg-red-50 p-4 rounded-lg">
                                <h3 class="font-bold text-red-600">핫 넘버 (Hot)</h3>
                                <p class="text-red-800 text-sm font-mono break-words">27,34,1,17,43,13,12,4,39,20,18,33,14,26,40</p>
                            </div>
                             <div class="bg-slate-50 p-4 rounded-lg">
                                <h3 class="font-bold text-slate-600">중립 넘버 (Neutral)</h3>
                                <p class="text-slate-800 text-sm font-mono break-words">5,7,8,11,15,16,21,24,25,31,35,36,38,45,10</p>
                            </div>
                            <div class="bg-blue-50 p-4 rounded-lg">
                                <h3 class="font-bold text-blue-600">쿨 넘버 (Cool)</h3>
                                <p class="text-blue-800 text-sm font-mono break-words">9,22,23,32,41,28,10,30,42,6,19,3,37,44,2</p>
                            </div>
                        </div>

                        <h3 class="text-xl font-bold text-slate-800 text-center mb-4">역대 당첨 조합 비율</h3>
                         <div class="chart-container">
                            <canvas id="hotCoolChart"></canvas>
                        </div>
                    </div>
                    <div class="bg-white p-6 rounded-xl shadow-md border border-slate-100">
                        <h2 class="text-2xl font-bold text-slate-900 mb-2">연속 번호 출현 패턴</h2>
                        <p class="text-slate-600 mb-6">역대 당첨 번호 중 연속된 번호(예: 15, 16)가 출현한 빈도를 번호대별로 분석합니다. 20번대와 30번대에서 비교적 자주 출현하는 경향을 보입니다.</p>
                         <div class="chart-container h-[400px] max-h-[450px]">
                            <canvas id="consecutiveChart"></canvas>
                        </div>
                    </div>
                </div>
                
                <!-- Methodology Content -->
                <div id="methodology-content" class="tab-pane hidden space-y-6">
                    <div class="bg-white p-6 rounded-xl shadow-md border border-slate-100">
                        <h3 class="text-xl font-bold text-slate-900 mb-3">1. 머신러닝 모델: LSTM</h3>
                        <p class="text-slate-600">로또 번호 예측의 복잡성을 고려하여, 시계열 데이터의 장기적 패턴 학습에 특화된 **LSTM(Long Short-Term Memory)** 모델을 이론적 최적 모델로 제안합니다. 이 모델은 단순 빈도 분석을 넘어, 회차별로 나타나는 번호 조합의 '순서'와 '패턴'을 학습하여 다음 회차에 나타날 가능성이 있는 번호의 특징을 예측하는 데 잠재력을 가집니다. 본 분석의 통계 필터링 과정에 LSTM 모델의 기본 원리를 일부 차용했습니다.</p>
                    </div>

                    <div class="bg-white p-6 rounded-xl shadow-md border border-slate-100">
                        <h3 class="text-xl font-bold text-slate-900 mb-3">2. 1187회차 오차 분석 및 모델 보정</h3>
                        <p class="text-slate-600 mb-4">지난 1187회차 예측(결과: 1개 번호 적중)을 복기한 결과, 천궁도 분석 시 행성의 '위치'에만 과도하게 집중한 것이 오차의 원인이었음을 확인했습니다. 행성 간의 '각도(Aspect)'와 하우스 '시작점(Cusp)'이라는 중요한 변수를 누락했습니다.</p>
                        <div class="bg-amber-50 border-l-4 border-amber-400 p-4 rounded-r-lg">
                            <p class="font-semibold text-amber-800">오차 보정 분석식:</p>
                            <p class="font-mono text-sm text-amber-900 mt-2">최종 번호 후보 = f(행성위치, 주요 각도 ± 오차, 하우스 시작점)</p>
                        </div>
                         <p class="text-slate-600 mt-4">이 새로운 보정식은 기존의 단일 차원적 분석에서 벗어나, 천체의 상호작용과 공간적 의미를 모두 고려하는 다차원적 접근법으로, 예측의 정확도를 높이는 것을 목표로 합니다.</p>
                    </div>

                    <div class="bg-white p-6 rounded-xl shadow-md border border-slate-100">
                        <h3 class="text-xl font-bold text-slate-900 mb-3">3. 0830 천궁도 재검증</h3>
                        <p class="text-slate-600 mb-4">위에서 제안된 보정 분석식을 1187회차(08.30) 천궁도에 다시 적용하여 유효성을 검증했습니다. 그 결과, 실제 당첨번호(`5, 13, 26, 29, 37, 40`)와 천궁도 요소들 간의 더 많은 유의미한 연결고리를 발견할 수 있었습니다.</p>
                        <div class="md:flex md:space-x-6 items-center">
                            <div class="md:w-2/3">
                                <ul class="list-disc list-inside text-slate-600 space-y-1 text-sm">
                                    <li><strong class="text-slate-800">번호 5, 13, 29:</strong> 각각 금성(5°), 달(13°), 천정(29°)의 위치와 정확히 일치.</li>
                                    <li><strong class="text-slate-800">번호 26, 40:</strong> 행성 간의 긴장 각도(90°, 180°)에서 파생된 번호로 해석 가능.</li>
                                    <li><strong class="text-slate-800">번호 37:</strong> 두 행성의 위치(7°, 30°)를 조합하여 생성된 번호로 해석 가능.</li>
                                </ul>
                            </div>
                            <div class="md:w-1/3 mt-4 md:mt-0 flex justify-center">
                                 <img src="0830.png" alt="2025년 8월 30일 천궁도" class="rounded-lg shadow-lg w-full max-w-[150px]">
                            </div>
                        </div>
                    </div>
                </div>
            </main>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const tabs = document.querySelectorAll('.tab-btn');
            const panes = document.querySelectorAll('.tab-pane');
            const tabNavigation = document.getElementById('tab-navigation');

            tabNavigation.addEventListener('click', (e) => {
                if (e.target.tagName === 'BUTTON') {
                    const tabId = e.target.dataset.tab;

                    tabs.forEach(tab => {
                        tab.classList.remove('active');
                    });
                    e.target.classList.add('active');

                    panes.forEach(pane => {
                        if (pane.id === `${tabId}-content`) {
                            pane.classList.remove('hidden');
                        } else {
                            pane.classList.add('hidden');
                        }
                    });
                }
            });

            // Chart Data
            const hotCoolData = {
                labels: ['2:2:2 (15.6%)', '3:2:1 (12.8%)', '2:3:1 (12.6%)', '1:3:2 (12.2%)', '3:1:2 (11.9%)', '기타'],
                datasets: [{
                    label: '조합 비율',
                    data: [185, 152, 149, 145, 141, 414],
                    backgroundColor: [
                        '#f59e0b', // amber-500
                        '#f97316', // orange-500
                        '#84cc16', // lime-500
                        '#10b981', // emerald-500
                        '#0ea5e9', // sky-500
                        '#64748b'  // slate-500
                    ],
                    hoverOffset: 4
                }]
            };

            const consecutiveData = {
                labels: ['1-10번대', '11-20번대', '21-30번대', '31-40번대', '41-45번대'],
                datasets: [
                    {
                        label: '2연속 번호 출현',
                        data: [125, 148, 162, 155, 38],
                        backgroundColor: '#38bdf8', // sky-400
                        borderColor: '#0ea5e9',
                        borderWidth: 1
                    },
                    {
                        label: '3연속 번호 출현',
                        data: [8, 11, 15, 12, 1],
                        backgroundColor: '#f87171', // red-400
                        borderColor: '#ef4444',
                        borderWidth: 1
                    }
                ]
            };

            // Chart Initialization
            const hotCoolCtx = document.getElementById('hotCoolChart');
            if(hotCoolCtx) {
                new Chart(hotCoolCtx, {
                    type: 'doughnut',
                    data: hotCoolData,
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        plugins: {
                            legend: {
                                position: 'top',
                            },
                            tooltip: {
                                callbacks: {
                                    label: function(context) {
                                        let label = context.label || '';
                                        if (label) {
                                            label += ': ';
                                        }
                                        if (context.parsed !== null) {
                                            label += context.raw.toLocaleString() + '회';
                                        }
                                        return label;
                                    }
                                }
                            }
                        }
                    },
                });
            }

            const consecutiveCtx = document.getElementById('consecutiveChart');
            if(consecutiveCtx) {
                new Chart(consecutiveCtx, {
                    type: 'bar',
                    data: consecutiveData,
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        scales: {
                            y: {
                                beginAtZero: true,
                                title: { display: true, text: '출현 횟수' }
                            }
                        },
                        plugins: {
                           legend: {
                                position: 'top',
                            },
                        }
                    }
                });
            }
        });
    </script>
</body>
</html>
