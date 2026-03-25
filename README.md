<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>珮誼工作室｜免費經營諮詢</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #f5ede8;
            font-family: 'Segoe UI', 'PingFang TC', 'Microsoft YaHei', Roboto, 'Helvetica Neue', sans-serif;
            padding: 1.5rem 1rem;
            color: #2c241f;
        }

        /* 主容器 */
        .form-card {
            max-width: 920px;
            margin: 0 auto;
            background: #ffffff;
            border-radius: 40px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08), 0 4px 12px rgba(0, 0, 0, 0.05);
            overflow: hidden;
        }

        /* 頭部 - 品牌區 */
        .hero {
            background: linear-gradient(135deg, #c28a6b 0%, #b06d4a 100%);
            padding: 2rem 2rem 1.8rem;
            text-align: center;
            color: white;
        }

        .hero h1 {
            font-size: 2.2rem;
            font-weight: 700;
            letter-spacing: 2px;
            margin-bottom: 0.3rem;
            text-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        .hero-badge {
            background: rgba(255,255,240,0.2);
            display: inline-block;
            padding: 0.3rem 1rem;
            border-radius: 40px;
            font-size: 0.85rem;
            font-weight: 500;
            margin-top: 8px;
            backdrop-filter: blur(4px);
        }

        .hero p {
            margin-top: 1rem;
            font-size: 0.95rem;
            opacity: 0.95;
        }

        /* 介紹區 */
        .intro {
            padding: 1.5rem 2rem 0.8rem;
            background: #fffbf8;
            border-bottom: 1px solid #f0e0d6;
        }

        .intro h2 {
            font-size: 1.5rem;
            color: #b26238;
            margin-bottom: 0.75rem;
            font-weight: 600;
        }

        .intro p {
            line-height: 1.5;
            color: #4a3529;
            margin-bottom: 0.75rem;
        }

        .highlight-tag {
            background: #f5e6de;
            padding: 0.2rem 0.6rem;
            border-radius: 20px;
            font-weight: 600;
            color: #b45a32;
            font-size: 0.85rem;
            display: inline-block;
        }

        .price-note {
            background: #fef0e8;
            border-left: 4px solid #c27752;
            padding: 0.8rem 1rem;
            border-radius: 20px;
            margin: 1rem 0 0.5rem;
            font-size: 0.9rem;
        }

        /* 表單區域 */
        form {
            padding: 1.2rem 2rem 2rem;
        }

        /* 問題區塊 */
        .question-block {
            margin-bottom: 1.8rem;
            border-bottom: 1px dashed #eedfd6;
            padding-bottom: 0.8rem;
        }

        .q-title {
            font-weight: 700;
            font-size: 1rem;
            margin-bottom: 0.6rem;
            display: flex;
            align-items: center;
            flex-wrap: wrap;
            gap: 8px;
            color: #3b2a21;
        }

        .q-num {
            background: #dcc2b2;
            width: 28px;
            height: 28px;
            border-radius: 30px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            font-weight: bold;
            color: #3a281f;
            margin-right: 6px;
        }

        .required {
            color: #c95a2a;
            font-size: 0.75rem;
            font-weight: normal;
            margin-left: 4px;
        }

        .sub-text {
            font-size: 0.7rem;
            color: #a88874;
            margin-top: 5px;
        }

        input, select, textarea {
            width: 100%;
            padding: 12px 18px;
            font-size: 0.9rem;
            border: 1.5px solid #e9dbd2;
            border-radius: 30px;
            background: #fefcfb;
            font-family: inherit;
            transition: 0.2s;
        }

        input:focus, select:focus, textarea:focus {
            border-color: #c88964;
            outline: none;
            box-shadow: 0 0 0 3px rgba(194, 122, 78, 0.15);
        }

        /* 複選/單選群組 改善間距 */
        .check-group, .radio-group {
            display: flex;
            flex-wrap: wrap;
            gap: 0.7rem 1.2rem;
            background: #fefaf7;
            padding: 0.8rem 1rem;
            border-radius: 28px;
            border: 1px solid #efdfd5;
            margin-top: 5px;
        }

        .check-group label, .radio-group label {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.88rem;
            font-weight: 500;
            cursor: pointer;
        }

        input[type="checkbox"], input[type="radio"] {
            width: 18px;
            height: 18px;
            accent-color: #b9623a;
            margin: 0;
        }

        .double-input {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }
        .double-input input {
            flex: 1;
            min-width: 130px;
        }

        hr {
            margin: 1rem 0;
            border: 0;
            height: 1px;
            background: linear-gradient(90deg, #eedbcb, #dbbcac, #eedbcb);
        }

        /* 提交按鈕 */
        .submit-btn {
            background: #b5582f;
            width: 100%;
            padding: 14px;
            font-size: 1.1rem;
            font-weight: bold;
            border: none;
            border-radius: 50px;
            color: white;
            cursor: pointer;
            transition: 0.2s;
            margin-top: 1rem;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        .submit-btn:hover {
            background: #9b461f;
            transform: translateY(-1px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.12);
        }

        .privacy-box {
            display: flex;
            align-items: center;
            gap: 10px;
            margin: 1.2rem 0 0.5rem;
            font-size: 0.8rem;
        }

        .privacy-box input {
            width: 18px;
            height: 18px;
        }

        .footer-note {
            background: #faf3ef;
            text-align: center;
            padding: 0.9rem;
            font-size: 0.7rem;
            color: #a6826a;
            border-top: 1px solid #f0dfd4;
        }

        @media (max-width: 600px) {
            .hero h1 { font-size: 1.8rem; }
            .intro h2 { font-size: 1.25rem; }
            form { padding: 1rem 1.2rem 1.5rem; }
            .check-group, .radio-group { gap: 0.5rem; }
            .q-title { font-size: 0.95rem; }
        }
    </style>
</head>
<body>
<div class="form-card">
    <div class="hero">
        <h1>珮誼工作室</h1>
        <div class="hero-badge">✦ 13年實戰美容東主 ✦ 創業陪跑導師 ✦</div>
        <p>半小時免費諮詢 · 為您釐清經營盲點</p>
    </div>

    <div class="intro">
        <h2>📋 精準需求訪談</h2>
        <p>您好，我是珮誼。走過13年獨資經營，從單打獨鬥到建立穩定團隊，<strong>更懂小型美容工作室的痛</strong>。若您正面臨<span class="highlight-tag">客源不穩</span>、<span class="highlight-tag">投資迷失</span>、<span class="highlight-tag">人員難管</span>、<span class="highlight-tag">定價困難</span>或<span class="highlight-tag">空置率高</span>，這30分鐘將是事業轉捩點。</p>
        <div class="price-note">
            💡 諮詢後將進一步說明 <strong>「經營管理班＋三個月陪跑變現」</strong>（價值$12,800），陪您將痛點轉為獲利引擎。
        </div>
    </div>

    <form action="https://formspree.io/f/xyknrnow" method="POST">
        <input type="hidden" name="_subject" value="珮誼工作室｜免費諮詢需求表單">
        
        <!-- 1. 基本資料 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">1</span> 基本資料 <span class="required">(必填)</span></div>
            <div class="double-input">
                <input type="text" name="姓名" placeholder="您的姓名／稱呼" required>
                <input type="email" name="電子郵件" placeholder="電子信箱 (寄送確認信)" required>
                <input type="tel" name="聯絡電話" placeholder="手機 / 電話 (選填)">
            </div>
            <div class="sub-text">請填寫常用信箱，諮詢安排將透過此信箱聯繫。</div>
        </div>

        <!-- 2. 美容事業狀態 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">2</span> 美容事業經營多久？<span class="required">(必填)</span></div>
            <select name="經營年資" required>
                <option value="" disabled selected>— 請選擇 —</option>
                <option>1年內 (籌備或剛起步)</option>
                <option>1-3年</option>
                <option>4-6年</option>
                <option>7-10年</option>
                <option>10年以上</option>
            </select>
        </div>

        <!-- 3. 團隊人數 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">3</span> 目前團隊總人數 (含自己) <span class="required">(必填)</span></div>
            <select name="團隊人數" required>
                <option value="" disabled selected>— 請選擇 —</option>
                <option>1人 (獨資經營／一人工作室)</option>
                <option>2-3人</option>
                <option>4-6人</option>
                <option>7-10人</option>
                <option>10人以上</option>
            </select>
        </div>

        <!-- 4. 痛點多選 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">4</span> 目前最困擾的經營問題 (可複選) <span class="required">(必填)</span></div>
            <div class="check-group">
                <label><input type="checkbox" name="痛點" value="未能找到新客"> 🔍 新客不足／預約率低</label>
                <label><input type="checkbox" name="痛點" value="投資欠缺方向"> 💰 投資方向模糊</label>
                <label><input type="checkbox" name="痛點" value="人員管理失當"> 👥 人員管理／流動率高</label>
                <label><input type="checkbox" name="痛點" value="價單難提升"> 💎 價單無法提升／利潤卡關</label>
                <label><input type="checkbox" name="痛點" value="投訴率高"> ⚠️ 客訴率高／服務糾紛</label>
                <label><input type="checkbox" name="痛點" value="難於聘請員工"> 🧑‍🤝‍🧑 招聘困難／缺工</label>
                <label><input type="checkbox" name="痛點" value="空置率高"> 📉 空置率高／產能閒置</label>
                <label><input type="checkbox" name="痛點" value="其他痛點"> 📝 其他 (請於下方說明)</label>
            </div>
            <input type="text" name="其他痛點敘述" placeholder="若勾選其他，請簡單描述 (例如：品牌定位、行銷轉換等)" style="margin-top: 10px;">
        </div>

        <!-- 5. 新客獲取 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">5</span> 每月新客數量狀況？</div>
            <select name="新客狀況">
                <option value="" disabled selected>— 請選擇 —</option>
                <option>幾乎無新客，僅靠熟客</option>
                <option>每月 1-3 位新客</option>
                <option>每月 4-8 位新客</option>
                <option>每月 9 位以上，但留存率低</option>
                <option>新客尚可，但客單價偏低</option>
            </select>
        </div>

        <!-- 6. 投資需求 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">6</span> 您覺得未來投資/資金運用上最需要哪方面協助？</div>
            <div class="radio-group">
                <label><input type="radio" name="投資協助" value="設備升級評估"> 設備升級評估</label>
                <label><input type="radio" name="投資協助" value="空間裝潢擴張"> 空間裝潢擴張</label>
                <label><input type="radio" name="投資協助" value="行銷廣告預算"> 行銷廣告預算配置</label>
                <label><input type="radio" name="投資協助" value="庫存成本控管"> 庫存/成本控管</label>
                <label><input type="radio" name="投資協助" value="還不確定"> 還不確定，想釐清方向</label>
            </div>
        </div>

        <!-- 7. 人員管理深入 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">7</span> 人員管理上最讓您頭痛的問題？(可複選)</div>
            <div class="check-group">
                <label><input type="checkbox" name="人員困擾" value="流動率高"> 💔 流動率高，培訓白費</label>
                <label><input type="checkbox" name="人員困擾" value="技術參差"> 🧴 員工技術參差不齊</label>
                <label><input type="checkbox" name="人員困擾" value="溝通摩擦"> 💬 團隊溝通摩擦/小團體</label>
                <label><input type="checkbox" name="人員困擾" value="業績消極"> 📊 缺乏業績動力/消極被動</label>
                <label><input type="checkbox" name="人員困擾" value="招聘困難"> 🚪 根本請不到適合的人</label>
            </div>
        </div>

        <!-- 8. 價單與定價 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">8</span> 關於價單升級/定價，您目前的情況？</div>
            <select name="定價困境">
                <option value="" disabled selected>— 請選擇 —</option>
                <option>客人常喊貴，不敢漲價</option>
                <option>低於行情，想調整但怕流失顧客</option>
                <option>想做高端服務，不懂價值包裝</option>
                <option>價單混亂，缺乏系統化設計</option>
                <option>目前價位尚可，但利潤未提升</option>
            </select>
        </div>

        <!-- 9. 客訴狀況 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">9</span> 近期是否有顧客抱怨或投訴？主要類型？</div>
            <textarea name="客訴描述" rows="2" placeholder="例如：效果不如預期、預約爭議、員工服務態度等，簡單說明即可"></textarea>
        </div>

        <!-- 10. 空置率/產能 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">10</span> 目前床位/美容師空置狀況？</div>
            <div class="radio-group">
                <label><input type="radio" name="空置率" value="經常滿約但新客不足"> 經常滿約，但新客不足</label>
                <label><input type="radio" name="空置率" value="空置率低於30%"> 空置率低於30% (尚可)</label>
                <label><input type="radio" name="空置率" value="空置率30%-50%"> 空置率30%-50% (產能浪費)</label>
                <label><input type="radio" name="空置率" value="空置率超過50%"> 空置率超過50% (嚴重)</label>
                <label><input type="radio" name="空置率" value="沒統計"> 沒特別統計</label>
            </div>
        </div>

        <!-- 11. 參加課程的核心期待 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">11</span> 若參加「經營管理班+陪跑」，最想達成的目標？<span class="required">(必填)</span></div>
            <textarea name="期待目標" rows="2" placeholder="例如：3個月內增加8個穩定會員、客單價提升25%、建立SOP降低投訴、打造團隊制度等…" required></textarea>
        </div>

        <!-- 12. 對課程的疑問 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">12</span> 對於$12,800經營管理班，您最想先了解的面向？</div>
            <textarea name="課程疑問" rows="2" placeholder="例如：課程架構、三個月陪跑具體方式、是否適合目前規模、課後輔導頻率等"></textarea>
        </div>

        <!-- 13. 額外補充 -->
        <div class="question-block">
            <div class="q-title"><span class="q-num">13</span> 其他想讓珮誼知道的經營現況？</div>
            <textarea name="補充現況" rows="2" placeholder="例如：主要服務項目、店面區域、現有行銷方式、近期瓶頸等"></textarea>
        </div>

        <!-- 隱私同意 -->
        <div class="privacy-box">
            <input type="checkbox" name="同意條款" value="同意" required>
            <label style="font-size:0.8rem;">我已閱讀並同意將以上資訊用於免費諮詢評估，並了解諮詢後可進一步了解經營管理班方案。</label>
        </div>

        <button type="submit" class="submit-btn">📩 預約半小時深度諮詢｜送出需求</button>
        <div class="sub-text" style="text-align:center; margin-top:12px;">✅ 提交後珮誼將於2個工作內回信，安排專屬諮詢時段</div>
    </form>

    <div class="footer-note">
        💬 13年實戰 x 陪跑式賦能 | 從一人工作室到穩定團隊，珮誼陪伴你突破經營天花板
    </div>
</div>
</body>
</html>
