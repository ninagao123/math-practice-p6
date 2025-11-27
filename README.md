# math-practice-p6
Primary 6 Math Volume &amp; Capacity Practice
<!DOCTYPE html>
<html lang="zh-HK">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>小六數學練習 - 體積與容量</title>
    <link rel="stylesheet" href="style.css">
    <link rel="icon" type="image/x-icon" href="assets/icons/favicon.ico">
</head>
<body>
    <!-- 导航栏 -->
    <nav class="navbar">
        <div class="nav-container">
            <h1 class="nav-logo">🎯 數學練習系統</h1>
            <div class="nav-stats">
                <span id="currentScore">得分: 0/0</span>
                <span id="progress">進度: 0%</span>
            </div>
        </div>
    </nav>

    <!-- 主内容区域 -->
    <main class="main-container">
        <!-- 欢迎页面 -->
        <section id="welcomePage" class="page active">
            <div class="welcome-card">
                <h2>歡迎來到數學練習系統！</h2>
                <div class="subject-info">
                    <h3>📚 練習範疇：體積與容量</h3>
                    <p>適合香港小學六年級學生</p>
                </div>
                
                <div class="features-list">
                    <div class="feature-item">
                        <span class="feature-icon">✅</span>
                        <span>選擇題與填空題練習</span>
                    </div>
                    <div class="feature-item">
                        <span class="feature-icon">📊</span>
                        <span>即時成績分析</span>
                    </div>
                    <div class="feature-item">
                        <span class="feature-icon">🔍</span>
                        <span>詳細題目解析</span>
                    </div>
                    <div class="feature-item">
                        <span class="feature-icon">📈</span>
                        <span>學習進度追蹤</span>
                    </div>
                </div>

                <div class="action-buttons">
                    <button class="btn-primary" onclick="startNewPractice()">
                        開始新練習
                    </button>
                    <button class="btn-secondary" onclick="showProgress()">
                        查看學習進度
                    </button>
                </div>
            </div>
        </section>

        <!-- 测验页面 -->
        <section id="quizPage" class="page">
            <div class="quiz-header">
                <h2>數學練習</h2>
                <div class="quiz-info">
                    <span id="questionCount">題目: 1/10</span>
                    <span id="timer">時間: 00:00</span>
                </div>
            </div>

            <div class="quiz-container">
                <div id="questionsContainer"></div>
                
                <div class="quiz-controls">
                    <button class="btn-secondary" onclick="previousQuestion()">
                        ← 上一題
                    </button>
                    <button class="btn-primary" onclick="nextQuestion()">
                        下一題 →
                    </button>
                    <button class="btn-success" onclick="submitQuiz()" id="submitBtn">
                        提交答案
                    </button>
                </div>
            </div>
        </section>

        <!-- 结果页面 -->
        <section id="resultsPage" class="page">
            <div class="results-card">
                <h2>練習結果</h2>
                
                <div class="score-display">
                    <div class="score-circle">
                        <span id="finalScore">0</span>
                        <small>分</small>
                    </div>
                    <div class="score-details">
                        <h3 id="performanceLevel">有待改進</h3>
                        <p>正確: <span id="correctCount">0</span>/<span id="totalCount">0</span></p>
                        <p>準確率: <span id="accuracy">0%</span></p>
                    </div>
                </div>

                <div class="results-details">
                    <div class="concept-breakdown">
                        <h4>概念掌握情況</h4>
                        <div id="conceptStats"></div>
                    </div>
                    
                    <div class="feedback-section">
                        <h4>題目解析</h4>
                        <div id="questionFeedback"></div>
                    </div>
                </div>

                <div class="results-actions">
                    <button class="btn-primary" onclick="startNewPractice()">
                        再次練習
                    </button>
                    <button class="btn-secondary" onclick="showWeakAreaPractice()">
                        弱項加強練習
                    </button>
                    <button class="btn-outline" onclick="showWelcomePage()">
                        返回主頁
                    </button>
                </div>
            </div>
        </section>

        <!-- 进度页面 -->
        <section id="progressPage" class="page">
            <div class="progress-card">
                <h2>學習進度</h2>
                
                <div class="progress-stats">
                    <div class="stat-item">
                        <span class="stat-value" id="totalPractices">0</span>
                        <span class="stat-label">總練習次數</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-value" id="averageScore">0%</span>
                        <span class="stat-label">平均得分</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-value" id="bestScore">0%</span>
                        <span class="stat-label">最佳成績</span>
                    </div>
                </div>

                <div class="progress-chart">
                    <h4>近期成績趨勢</h4>
                    <canvas id="progressChart" width="400" height="200"></canvas>
                </div>

                <div class="weak-areas">
                    <h4>需要加強的概念</h4>
                    <div id="weakAreasList"></div>
                </div>

                <div class="progress-actions">
                    <button class="btn-primary" onclick="clearProgress()">
                        清除進度
                    </button>
                    <button class="btn-outline" onclick="showWelcomePage()">
                        返回主頁
                    </button>
                </div>
            </div>
        </section>
    </main>

    <!-- JavaScript 文件 -->
    <script src="questions.js"></script>
    <script src="script.js"></script>
</body>
</html>
