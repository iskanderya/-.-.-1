
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Александра, у меня есть предложение 💙</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', sans-serif; }
  body {
    min-height: 100vh;
    background: linear-gradient(135deg, #a1c4fd 0%, #c2e9fb 50%, #89f7fe 100%);
    display: flex;
    justify-content: center;
    align-items: center;
    overflow-x: hidden;
    padding: 20px;
    position: relative;
  }
  .card {
    background: rgba(255, 255, 255, 0.97);
    padding: 35px 30px;
    border-radius: 25px;
    box-shadow: 0 20px 60px rgba(2, 136, 209, 0.15);
    text-align: center;
    max-width: 600px;
    width: 100%;
    z-index: 10;
    animation: pop 0.8s ease-out;
  }
  @keyframes pop {
    0% { transform: scale(0.5); opacity: 0; }
    100% { transform: scale(1); opacity: 1; }
  }
  h1 { font-size: 2em; color: #0288d1; margin-bottom: 10px; }
  .name {
    background: linear-gradient(135deg, #0288d1, #03a9f4);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    font-weight: bold;
  }
  .subtitle { font-size: 1.1em; color: #546e7a; margin-bottom: 25px; }
  .step-label {
    display: inline-block;
    background: #e1f5fe;
    color: #0288d1;
    padding: 5px 14px;
    border-radius: 20px;
    font-size: 0.85em;
    font-weight: 600;
    margin-bottom: 15px;
  }
  
  .days-menu {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    gap: 6px;
    margin-bottom: 20px;
  }
  .day-btn {
    padding: 10px 4px;
    border: 2px solid #b3e5fc;
    background: white;
    border-radius: 12px;
    cursor: pointer;
    font-size: 0.85em;
    font-weight: 600;
    color: #78909c;
    transition: all 0.3s;
  }
  .day-btn:hover { transform: translateY(-3px); border-color: #4facfe; color: #0288d1; }
  .day-btn.active {
    background: linear-gradient(135deg, #4facfe, #00f2fe);
    color: white;
    border-color: transparent;
    box-shadow: 0 5px 15px rgba(79, 172, 254, 0.4);
  }
  
  .day-content {
    background: linear-gradient(135deg, #e1f5fe, #b3e5fc);
    padding: 20px;
    border-radius: 18px;
    margin-bottom: 20px;
    animation: slideIn 0.4s ease-out;
  }
  @keyframes slideIn {
    0% { opacity: 0; transform: translateY(15px); }
    100% { opacity: 1; transform: translateY(0); }
  }
  .day-icon { font-size: 40px; margin-bottom: 8px; }
  .day-title { font-size: 1.2em; color: #0288d1; margin-bottom: 6px; font-weight: bold; }
  .day-desc { color: #546e7a; line-height: 1.5; font-size: 0.95em; }
  
  .activity-section, .location-section, .restaurant-section, .walk-section, .fun-section, .dishes-section, .comment-section {
    animation: slideIn 0.5s ease-out;
    margin-bottom: 20px;
  }
  .activity-options, .location-options, .restaurant-options, .walk-options, .fun-options, .dishes-options {
    display: grid;
    gap: 10px;
  }
  .activity-options { grid-template-columns: repeat(3, 1fr); }
  .location-options, .walk-options, .restaurant-options { grid-template-columns: repeat(2, 1fr); }
  .fun-options { grid-template-columns: repeat(3, 1fr); }
  .dishes-options { grid-template-columns: repeat(3, 1fr); }
  
  .activity-card, .location-card, .restaurant-card, .walk-card, .fun-card, .dish-card {
    background: white;
    border: 2px solid #b3e5fc;
    border-radius: 16px;
    padding: 15px 10px;
    cursor: pointer;
    transition: all 0.3s;
    text-align: center;
  }
  .activity-card:hover, .location-card:hover, .restaurant-card:hover, .walk-card:hover, .fun-card:hover, .dish-card:hover {
    transform: translateY(-5px);
    border-color: #4facfe;
    box-shadow: 0 8px 20px rgba(79, 172, 254, 0.2);
  }
  .activity-card.active, .location-card.active, .restaurant-card.active, .walk-card.active, .fun-card.active, .dish-card.active {
    background: linear-gradient(135deg, #4facfe, #00f2fe);
    border-color: transparent;
    color: white;
    box-shadow: 0 8px 20px rgba(79, 172, 254, 0.4);
  }
  .activity-card .a-icon, .location-card .l-icon, .restaurant-card .r-icon, .walk-card .w-icon, .fun-card .f-icon, .dish-card .d-icon {
    font-size: 28px;
    margin-bottom: 6px;
  }
  .activity-card .a-name, .location-card .l-name, .restaurant-card .r-name, .walk-card .w-name, .fun-card .f-name, .dish-card .d-name {
    font-size: 0.9em;
    font-weight: 600;
    color: #546e7a;
  }
  .activity-card.active .a-name, .location-card.active .l-name, .restaurant-card.active .r-name, .walk-card.active .w-name, .fun-card.active .f-name, .dish-card.active .d-name { color: white; }
  
  .activity-details, .location-details, .restaurant-details, .walk-details, .fun-details, .dishes-summary {
    background: linear-gradient(135deg, #e1f5fe, #b3e5fc);
    padding: 18px;
    border-radius: 15px;
    margin-top: 15px;
    text-align: left;
    animation: slideIn 0.4s ease-out;
  }
  .activity-details p, .location-details p, .restaurant-details p, .walk-details p, .fun-details p, .dishes-summary p {
    color: #546e7a;
    line-height: 1.5;
    font-size: 0.95em;
    margin-bottom: 8px;
  }
  .time-tag {
    display: inline-block;
    background: white;
    padding: 5px 12px;
    border-radius: 20px;
    font-size: 0.85em;
    color: #0288d1;
    font-weight: 600;
  }
  
  .dishes-summary .hint {
    font-size: 0.85em;
    color: #78909c;
    font-style: italic;
    margin-bottom: 10px;
  }
  .dishes-list {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 10px;
  }
  .dish-tag {
    background: white;
    color: #0288d1;
    padding: 6px 12px;
    border-radius: 20px;
    font-size: 0.9em;
    font-weight: 600;
    border: 1px solid #b3e5fc;
    animation: slideIn 0.3s ease-out;
  }
  .empty-dishes {
    color: #78909c;
    font-style: italic;
    font-size: 0.9em;
    margin-top: 8px;
  }
  
  .custom-input {
    width: 100%;
    padding: 10px 15px;
    border: 2px solid #b3e5fc;
    border-radius: 12px;
    font-family: 'Segoe UI', sans-serif;
    font-size: 0.95em;
    color: #546e7a;
    background: white;
    margin-top: 10px;
    outline: none;
    transition: all 0.3s;
  }
  .custom-input:focus {
    border-color: #4facfe;
    box-shadow: 0 0 0 3px rgba(79, 172, 254, 0.15);
  }
  
  .comment-section {
    background: linear-gradient(135deg, #e1f5fe, #b3e5fc);
    padding: 20px;
    border-radius: 18px;
    text-align: left;
    border: 2px dashed #b3e5fc;
  }
  .comment-section .comment-label {
    display: flex;
    align-items: center;
    gap: 8px;
    color: #0288d1;
    font-weight: 600;
    font-size: 1em;
    margin-bottom: 10px;
  }
  .comment-section .comment-hint {
    font-size: 0.85em;
    color: #78909c;
    font-style: italic;
    margin-bottom: 12px;
    line-height: 1.4;
  }
  .comment-input {
    width: 100%;
    min-height: 90px;
    padding: 12px 15px;
    border: 2px solid #b3e5fc;
    border-radius: 14px;
    font-family: 'Segoe UI', sans-serif;
    font-size: 0.95em;
    color: #546e7a;
    background: white;
    resize: vertical;
    transition: all 0.3s;
    outline: none;
  }
  .comment-input:focus {
    border-color: #4facfe;
    box-shadow: 0 0 0 3px rgba(79, 172, 254, 0.15);
  }
  .comment-input::placeholder { color: #b0bec5; font-style: italic; }
  .char-counter {
    text-align: right;
    font-size: 0.8em;
    color: #90a4ae;
    margin-top: 6px;
  }
  
  .buttons { display: flex; gap: 12px; justify-content: center; flex-wrap: wrap; margin-top: 25px; }
  button.action {
    padding: 13px 30px;
    font-size: 1.05em;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    transition: all 0.3s;
    font-weight: bold;
  }
  .yes {
    background: linear-gradient(135deg, #4facfe, #00f2fe);
    color: white;
    box-shadow: 0 5px 15px rgba(79, 172, 254, 0.4);
  }
  .yes:hover { transform: scale(1.08); box-shadow: 0 8px 20px rgba(79, 172, 254, 0.6); }
  .yes:disabled {
    opacity: 0.7;
    cursor: not-allowed;
    transform: none;
  }
  .back {
    background: white;
    color: #0288d1;
    border: 2px solid #b3e5fc;
  }
  .back:hover { background: #e1f5fe; }
  .no {
    background: #eceff1;
    color: #78909c;
    position: relative;
    transition: all 0.2s;
  }
  
  .sending-indicator {
    display: none;
    margin-top: 15px;
    padding: 10px 20px;
    background: #e1f5fe;
    border-radius: 20px;
    color: #0288d1;
    font-size: 0.9em;
    font-weight: 600;
    animation: pulse 1.5s infinite;
  }
  .sending-indicator.active { display: inline-block; }
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.5; }
  }
  
  .heart {
    position: fixed;
    font-size: 24px;
    animation: fall linear forwards;
    pointer-events: none;
    user-select: none;
    z-index: 1;
  }
  @keyframes fall {
    0% { transform: translateY(-100vh) rotate(0deg); opacity: 1; }
    100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
  }
  
  .success { display: none; animation: pop 0.6s ease-out; }
  .success h1 { font-size: 2.2em; margin-bottom: 15px; }
  .big-heart {
    font-size: 80px;
    animation: beat 1s infinite;
    display: inline-block;
  }
  @keyframes beat {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.2); }
  }
  .chosen-info {
    background: linear-gradient(135deg, #e1f5fe, #b3e5fc);
    padding: 20px;
    border-radius: 15px;
    margin: 20px 0;
    border-left: 4px solid #4facfe;
    text-align: left;
  }
  .chosen-info p { margin: 6px 0; color: #546e7a; }
  .chosen-info strong { color: #0288d1; }
  .chosen-info .dish-tag {
    background: white;
    color: #0288d1;
    padding: 4px 10px;
    border-radius: 15px;
    font-size: 0.85em;
    font-weight: 600;
    display: inline-block;
    margin: 3px 3px 3px 0;
  }
  .chosen-info .comment-block {
    background: white;
    padding: 14px 16px;
    border-radius: 12px;
    margin-top: 12px;
    border-left: 3px solid #4facfe;
    font-style: italic;
    color: #546e7a;
    line-height: 1.5;
  }
  .chosen-info .comment-block::before {
    content: '💬 ';
    font-style: normal;
  }
  .paws-message {
    margin-top: 20px;
    padding: 15px;
    background: linear-gradient(135deg, #e3f2fd, #bbdefb);
    border-radius: 15px;
    color: #0277bd;
    font-size: 1.05em;
    font-weight: 600;
    line-height: 1.5;
    border: 2px solid #90caf9;
    animation: pulse 2s infinite;
  }
  .sheet-status {
    margin-top: 15px;
    padding: 10px 15px;
    border-radius: 12px;
    font-size: 0.85em;
    font-weight: 600;
  }
  .sheet-status.success { background: #e8f5e9; color: #2e7d32; }
  .sheet-status.error { background: #ffebee; color: #c62828; }
  
  @media (max-width: 500px) {
    .days-menu { grid-template-columns: repeat(4, 1fr); }
    .activity-options, .location-options, .restaurant-options, .walk-options, .fun-options, .dishes-options { grid-template-columns: repeat(2, 1fr); }
    h1 { font-size: 1.6em; }
    .card { padding: 25px 18px; }
  }
</style>
</head>
<body>

<div class="card" id="mainCard">
  <h1>Привет, <span class="name">Александра</span> 💙</h1>
  <p class="subtitle">Давай спланируем наше идеальное свидание ✨</p>

  <div class="step-label">Шаг 1 · Выбери день</div>
  <div class="days-menu" id="daysMenu">
    <button class="day-btn active" data-day="mon">Пн</button>
    <button class="day-btn" data-day="tue">Вт</button>
    <button class="day-btn" data-day="wed">Ср</button>
    <button class="day-btn" data-day="thu">Чт</button>
    <button class="day-btn" data-day="fri">Пт</button>
    <button class="day-btn" data-day="sat">Сб</button>
    <button class="day-btn" data-day="sun">Вс</button>
  </div>
  <div class="day-content" id="dayContent"></div>

  <div class="activity-section" id="activitySection">
    <div class="step-label">Шаг 2 · Что будем делать?</div>
    <div class="activity-options" id="activityOptions">
      <div class="activity-card" data-act="dinner"><div class="a-icon">🍽️</div><div class="a-name">Поужинаем</div></div>
      <div class="activity-card" data-act="walk"><div class="a-icon">🌳</div><div class="a-name">Погуляем</div></div>
      <div class="activity-card" data-act="fun"><div class="a-icon">🎉</div><div class="a-name">Развлечёмся</div></div>
    </div>
    <div id="activityDetails"></div>
  </div>

  <div class="location-section" id="locationSection" style="display: none;">
    <div class="step-label">Шаг 3 · Где поужинаем?</div>
    <div class="location-options" id="locationOptions">
      <div class="location-card" data-loc="home"><div class="l-icon">🏠</div><div class="l-name">Дома</div></div>
      <div class="location-card" data-loc="restaurant"><div class="l-icon">🍷</div><div class="l-name">В ресторане</div></div>
    </div>
    <div id="locationDetails"></div>
  </div>

  <div class="restaurant-section" id="restaurantSection" style="display: none;">
    <div class="step-label">Шаг 3б · Выбери ресторан</div>
    <div class="restaurant-options" id="restaurantOptions">
      <div class="restaurant-card" data-rest="byk"><div class="r-icon">🥩</div><div class="r-name">Бык</div></div>
      <div class="restaurant-card" data-rest="bernice"><div class="r-icon">🍹</div><div class="r-name">Бернис</div></div>
      <div class="restaurant-card" data-rest="barbados"><div class="r-icon">🏝️</div><div class="r-name">Барбадос</div></div>
      <div class="restaurant-card" data-rest="berimore"><div class="r-icon">🎩</div><div class="r-name">Бэримор</div></div>
      <div class="restaurant-card" data-rest="london"><div class="r-icon">🇬🇧</div><div class="r-name">Лондон</div></div>
      <div class="restaurant-card" data-rest="custom"><div class="r-icon">✏️</div><div class="r-name">Свой вариант</div></div>
    </div>
    <div id="restaurantDetails"></div>
    <input type="text" id="customRestaurantInput" class="custom-input" placeholder="Напиши название места..." style="display: none;" oninput="updateCustomRestaurant()">
  </div>

  <div class="walk-section" id="walkSection" style="display: none;">
    <div class="step-label">Шаг 3 · Куда пойдём гулять?</div>
    <div class="walk-options" id="walkOptions">
      <div class="walk-card" data-walk="embankment"><div class="w-icon">🌊</div><div class="w-name">На набережную</div></div>
      <div class="walk-card" data-walk="park"><div class="w-icon">🌲</div><div class="w-name">В парк</div></div>
    </div>
    <div id="walkDetails"></div>
  </div>

  <div class="fun-section" id="funSection" style="display: none;">
    <div class="step-label">Шаг 3 · Куда пойдем развлекаться?</div>
    <div class="fun-options" id="funOptions">
      <div class="fun-card" data-fun="pottery"><div class="f-icon">🏺</div><div class="f-name">Гончарная мастерская</div></div>
      <div class="fun-card" data-fun="ropes"><div class="f-icon">🧗</div><div class="f-name">Веревочный парк</div></div>
      <div class="fun-card" data-fun="museum"><div class="f-icon">🏛️</div><div class="f-name">Музей</div></div>
      <div class="fun-card" data-fun="cinema"><div class="f-icon">🎬</div><div class="f-name">Кино</div></div>
      <div class="fun-card" data-fun="theater"><div class="f-icon">🎭</div><div class="f-name">Театр</div></div>
    </div>
    <div id="funDetails"></div>
  </div>

  <div class="dishes-section" id="dishesSection" style="display: none;">
    <div class="step-label">Шаг 4 · Что приготовлю? (можно выбрать несколько)</div>
    <div class="dishes-options" id="dishesOptions">
      <div class="dish-card" data-dish="meat"><div class="d-icon">🥩</div><div class="d-name">Мясо</div></div>
      <div class="dish-card" data-dish="fish"><div class="d-icon">🐟</div><div class="d-name">Рыба</div></div>
      <div class="dish-card" data-dish="chicken"><div class="d-icon">🍗</div><div class="d-name">Курица / Индейка</div></div>
      <div class="dish-card" data-dish="olivier"><div class="d-icon">🥗</div><div class="d-name">Салат Оливье</div></div>
      <div class="dish-card" data-dish="shrimp"><div class="d-icon">🍤</div><div class="d-name">Креветочный Балдеж</div></div>
      <div class="dish-card" data-dish="funchoza"><div class="d-icon">🥢</div><div class="d-name">Салат с Фунчозой</div></div>
      <div class="dish-card" data-dish="caprice"><div class="d-icon">🥗</div><div class="d-name">Мужской Каприз</div></div>
      <div class="dish-card" data-dish="tuna"><div class="d-icon">🐟</div><div class="d-name">Салат с тунцом</div></div>
      <div class="dish-card" data-dish="enoki"><div class="d-icon">🍄</div><div class="d-name">Эноки в Беконе</div></div>
    </div>
    <div class="dishes-summary" id="dishesSummary">
      <p class="hint">💡 Кликай по блюдам — можно выбрать несколько</p>
      <p><strong>Твой выбор:</strong></p>
      <div class="dishes-list" id="dishesList">
        <span class="empty-dishes">Пока ничего не выбрано</span>
      </div>
    </div>
  </div>

  <div class="comment-section">
    <div class="comment-label">💬 Оставь пожелание или комментарий</div>
    <div class="comment-hint">Можешь написать что угодно: аллергии, предпочтения, или просто тёплые слова — я всё учту 💙</div>
    <textarea id="commentInput" class="comment-input" placeholder="Например: не ем лук, или просто «люблю тебя» 💙" maxlength="300" oninput="updateCharCounter()"></textarea>
    <div class="char-counter"><span id="charCount">0</span> / 300</div>
  </div>

  <div class="buttons">
    <button class="action back" onclick="goBack()">← Назад</button>
    <button class="action yes" id="yesBtn" onclick="sayYes()">Да, я согласна 💖</button>
    <button class="action no" id="noBtn" onmouseover="runAway()" onclick="runAway()">Нет</button>
  </div>
  <div class="sending-indicator" id="sendingIndicator">💌 Сохраняем твой выбор...</div>
</div>

<div class="card success" id="successCard">
  <div class="big-heart">💙</div>
  <h1>Сашенька, ура!</h1>
  <p>Я безумно рад, что ты согласилась 🌹</p>
  <div class="chosen-info" id="chosenInfo"></div>
  
  <div class="paws-message">
    🐾 А после свидания тебе будет предложено пожамкать лапки и посмотреть сериал 📺💙
  </div>
  
  <div id="sheetStatus"></div>
  <p style="margin-top: 15px;">Обещаю, это будет волшебный вечер ✨</p>
</div>

<script>
  const GOOGLE_SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbz97D2fm60BbT5cqpqKA1pS4xpUQDtq-jyPKAUQo9MyGeWA2KGpbd4NMWPnwXY9M8pS/exec';

  const daysData = {
    mon: { icon: '🌙', title: 'Понедельник', desc: 'Начнём неделю красиво' },
    tue: { icon: '✨', title: 'Вторник', desc: 'Маленький праздник среди недели' },
    wed: { icon: '☕', title: 'Среда', desc: 'Перерыв на самое важное' },
    thu: { icon: '🌟', title: 'Четверг', desc: 'Предвкушение выходных' },
    fri: { icon: '🥂', title: 'Пятница', desc: 'Начало лучших выходных' },
    sat: { icon: '💙', title: 'Суббота', desc: 'Целый день только для нас' },
    sun: { icon: '🥐', title: 'Воскресенье', desc: 'Нежное начало недели' }
  };

  const activitiesData = {
    dinner: { icon: '🍽️', name: 'Ужин', desc: 'Устроим романтический вечер за вкусной едой и приятными разговорами.', time: '20:00' },
    walk: { icon: '🌳', name: 'Прогулка', desc: 'Свежий воздух, красивые виды и долгие разговоры — что может быть лучше?', time: '18:00' },
    fun: { icon: '🎉', name: 'Развлечения', desc: 'Выберем то, от чего горят глаза. Будет весело и незабываемо, обещаю!', time: '18:00' }
  };

  const locationsData = {
    home: { icon: '🏠', name: 'Дома', desc: 'Приготовлю что-то особенное. Свечи, музыка, уютная атмосфера — только мы вдвоём.', time: '19:30' },
    restaurant: { icon: '🍷', name: 'В ресторане', desc: 'Забронирую столик в уютном месте. Приглушённый свет, вкусная еда и долгие разговоры.', time: '20:00' }
  };

  const restaurantData = {
    byk: { icon: '🥩', name: 'Бык', desc: 'Сочные стейки и мясные деликатесы в отличной атмосфере' },
    bernice: { icon: '🍹', name: 'Бернис', desc: 'Уютная атмосфера, отличная кухня и напитки' },
    barbados: { icon: '🏝️', name: 'Барбадос', desc: 'Яркие вкусы и расслабленная тропическая атмосфера' },
    berimore: { icon: '🎩', name: 'Бэримор', desc: 'Элегантный интерьер и изысканная подача блюд' },
    london: { icon: '🇬🇧', name: 'Лондон', desc: 'Английский стиль, классические блюда и особый шарм' },
    custom: { icon: '✏️', name: 'Свой вариант', desc: 'Напиши место, о котором ты мечтаешь пойти' }
  };

  const walkData = {
    embankment: { icon: '🌊', name: 'На набережную', desc: 'Прогуляемся вдоль воды, посмотрим на закат, возьмём кофе на вынос. Романтика в чистом виде 💫', time: '18:30' },
    park: { icon: '🌲', name: 'В парк', desc: 'Тенистые аллеи, свежий воздух. Можно покормить уток, покататься на катамаране или просто болтать 🍃', time: '17:00' }
  };

  const funData = {
    pottery: { icon: '🏺', name: 'Гончарная мастерская', desc: 'Слепим что-нибудь красивое своими руками. Это очень сближает!', time: '18:00' },
    ropes: { icon: '🧗', name: 'Веревочный парк', desc: 'Немного адреналина, свежий воздух и командная поддержка!', time: '16:00' },
    museum: { icon: '🏛️', name: 'Музей', desc: 'Погрузимся в искусство. А потом обсудим впечатления за чашкой кофе.', time: '17:00' },
    cinema: { icon: '🎬', name: 'Кино', desc: 'Посмотрим крутую новинку. С большим попкорном и обнимашками.', time: '19:00' },
    theater: { icon: '🎭', name: 'Театр', desc: 'Вечер высокой культуры, красивых костюмов и сильных эмоций.', time: '19:00' }
  };

  const dishesData = {
    meat: { icon: '🥩', name: 'Мясо', desc: 'Сочный стейк или нежная вырезка' },
    fish: { icon: '🐟', name: 'Рыба', desc: 'Запечённая рыба с травами и лимоном' },
    chicken: { icon: '🍗', name: 'Курица / Индейка', desc: 'Нежная грудка в соусе' },
    olivier: { icon: '🥗', name: 'Салат Оливье', desc: 'Классика, которую все любят' },
    shrimp: { icon: '🍤', name: 'Креветочный Балдеж', desc: 'Тигровые креветки в чесночном масле' },
    funchoza: { icon: '🥢', name: 'Салат с Фунчозой', desc: 'Стеклянная лапша с овощами' },
    caprice: { icon: '🥗', name: 'Мужской Каприз', desc: 'Сытный салат с мясом и грибами' },
    tuna: { icon: '🐟', name: 'Салат с тунцом', desc: 'Лёгкий салат с тунцом и овощами' },
    enoki: { icon: '🍄', name: 'Эноки в Беконе', desc: 'Грибы эноки в хрустящем беконе' }
  };

  let currentDay = 'mon';
  let currentActivity = null;
  let currentLocation = null;
  let currentRestaurant = null;
  let customRestaurantName = '';
  let currentWalk = null;
  let currentFun = null;
  let currentDishes = [];

  function renderDay(dayKey) {
    currentDay = dayKey;
    const data = daysData[dayKey];
    const content = document.getElementById('dayContent');
    content.style.animation = 'none'; void content.offsetWidth;
    content.style.animation = 'slideIn 0.4s ease-out';
    content.innerHTML = `<div class="day-icon">${data.icon}</div><div class="day-title">${data.title}</div><div class="day-desc">${data.desc}</div>`;
    resetAll();
  }

  function resetAll() {
    currentActivity = null; currentLocation = null; currentRestaurant = null; customRestaurantName = '';
    currentWalk = null; currentFun = null; currentDishes = [];
    document.querySelectorAll('.activity-card, .location-card, .restaurant-card, .walk-card, .fun-card, .dish-card').forEach(c => c.classList.remove('active'));
    document.getElementById('activityDetails').innerHTML = '';
    document.getElementById('locationSection').style.display = 'none';
    document.getElementById('locationDetails').innerHTML = '';
    document.getElementById('restaurantSection').style.display = 'none';
    document.getElementById('restaurantDetails').innerHTML = '';
    document.getElementById('customRestaurantInput').style.display = 'none';
    document.getElementById('customRestaurantInput').value = '';
    document.getElementById('walkSection').style.display = 'none';
    document.getElementById('walkDetails').innerHTML = '';
    document.getElementById('funSection').style.display = 'none';
    document.getElementById('funDetails').innerHTML = '';
    document.getElementById('dishesSection').style.display = 'none';
    renderDishesList();
  }

  function renderActivity(actKey) {
    currentActivity = actKey;
    const data = activitiesData[actKey];
    const details = document.getElementById('activityDetails');
    details.style.animation = 'none'; void details.offsetWidth;
    details.style.animation = 'slideIn 0.4s ease-out';
    details.innerHTML = `<div class="activity-details"><p><strong>${data.icon} ${data.name}:</strong> ${data.desc}</p><span class="time-tag">🕐 ${daysData[currentDay].title} в ${data.time}</span></div>`;
    
    currentLocation = null; currentRestaurant = null; customRestaurantName = ''; currentWalk = null; currentFun = null; currentDishes = [];
    document.querySelectorAll('.location-card, .restaurant-card, .walk-card, .fun-card, .dish-card').forEach(c => c.classList.remove('active'));
    document.getElementById('locationDetails').innerHTML = '';
    document.getElementById('restaurantDetails').innerHTML = '';
    document.getElementById('customRestaurantInput').style.display = 'none';
    document.getElementById('customRestaurantInput').value = '';
    document.getElementById('walkDetails').innerHTML = '';
    document.getElementById('funDetails').innerHTML = '';
    renderDishesList();
    
    document.getElementById('locationSection').style.display = (actKey === 'dinner') ? 'block' : 'none';
    document.getElementById('restaurantSection').style.display = 'none';
    document.getElementById('walkSection').style.display = (actKey === 'walk') ? 'block' : 'none';
    document.getElementById('funSection').style.display = (actKey === 'fun') ? 'block' : 'none';
    document.getElementById('dishesSection').style.display = 'none';
  }

  function renderDetails(type, key, dataObj, containerId) {
    if (type === 'location') currentLocation = key;
    if (type === 'restaurant') currentRestaurant = key;
    if (type === 'walk') currentWalk = key;
    if (type === 'fun') currentFun = key;
    
    const data = dataObj[key];
    const details = document.getElementById(containerId);
    details.style.animation = 'none'; void details.offsetWidth;
    details.style.animation = 'slideIn 0.4s ease-out';
    details.innerHTML = `<div class="${type}-details"><p><strong>${data.icon} ${data.name}:</strong> ${data.desc}</p><span class="time-tag">🕐 ${daysData[currentDay].title} в ${data.time}</span></div>`;
    
    if (type === 'location' && key === 'home') {
      document.getElementById('dishesSection').style.display = 'block';
      document.getElementById('restaurantSection').style.display = 'none';
    } else if (type === 'location' && key === 'restaurant') {
      document.getElementById('restaurantSection').style.display = 'block';
      document.getElementById('dishesSection').style.display = 'none';
      currentDishes = [];
      document.querySelectorAll('.dish-card').forEach(c => c.classList.remove('active'));
      renderDishesList();
    } else if (type === 'location') {
      document.getElementById('restaurantSection').style.display = 'none';
      document.getElementById('dishesSection').style.display = 'none';
    }
  }

  function updateCustomRestaurant() {
    customRestaurantName = document.getElementById('customRestaurantInput').value.trim();
  }

  function toggleDish(dishKey) {
    const idx = currentDishes.indexOf(dishKey);
    if (idx > -1) currentDishes.splice(idx, 1);
    else currentDishes.push(dishKey);
    renderDishesList();
  }

  function renderDishesList() {
    const list = document.getElementById('dishesList');
    if (currentDishes.length === 0) {
      list.innerHTML = '<span class="empty-dishes">Пока ничего не выбрано</span>';
      return;
    }
    list.innerHTML = currentDishes.map(key => {
      const d = dishesData[key];
      return `<span class="dish-tag">${d.icon} ${d.name}</span>`;
    }).join('');
  }

  function updateCharCounter() {
    const input = document.getElementById('commentInput');
    document.getElementById('charCount').textContent = input.value.length;
  }

  document.querySelectorAll('.day-btn').forEach(btn => btn.addEventListener('click', () => {
    document.querySelectorAll('.day-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active'); renderDay(btn.dataset.day);
  }));

  document.querySelectorAll('.activity-card').forEach(card => card.addEventListener('click', () => {
    document.querySelectorAll('.activity-card').forEach(c => c.classList.remove('active'));
    card.classList.add('active'); renderActivity(card.dataset.act);
  }));

  document.querySelectorAll('.location-card').forEach(card => card.addEventListener('click', () => {
    document.querySelectorAll('.location-card').forEach(c => c.classList.remove('active'));
    card.classList.add('active'); renderDetails('location', card.dataset.loc, locationsData, 'locationDetails');
  }));

  document.querySelectorAll('.restaurant-card').forEach(card => card.addEventListener('click', () => {
    document.querySelectorAll('.restaurant-card').forEach(c => c.classList.remove('active'));
    card.classList.add('active'); renderDetails('restaurant', card.dataset.rest, restaurantData, 'restaurantDetails');
    
    const customInput = document.getElementById('customRestaurantInput');
    if (card.dataset.rest === 'custom') {
      customInput.style.display = 'block';
      customInput.focus();
    } else {
      customInput.style.display = 'none';
      customRestaurantName = '';
      customInput.value = '';
    }
  }));

  document.querySelectorAll('.walk-card').forEach(card => card.addEventListener('click', () => {
    document.querySelectorAll('.walk-card').forEach(c => c.classList.remove('active'));
    card.classList.add('active'); renderDetails('walk', card.dataset.walk, walkData, 'walkDetails');
  }));

  document.querySelectorAll('.fun-card').forEach(card => card.addEventListener('click', () => {
    document.querySelectorAll('.fun-card').forEach(c => c.classList.remove('active'));
    card.classList.add('active'); renderDetails('fun', card.dataset.fun, funData, 'funDetails');
  }));

  document.querySelectorAll('.dish-card').forEach(card => card.addEventListener('click', () => {
    card.classList.toggle('active');
    toggleDish(card.dataset.dish);
  }));

  function goBack() {
    if (currentDishes.length > 0) {
      currentDishes = [];
      document.querySelectorAll('.dish-card').forEach(c => c.classList.remove('active'));
      renderDishesList();
    } else if (currentRestaurant) {
      currentRestaurant = null; customRestaurantName = '';
      document.querySelectorAll('.restaurant-card').forEach(c => c.classList.remove('active'));
      document.getElementById('restaurantDetails').innerHTML = '';
      document.getElementById('customRestaurantInput').style.display = 'none';
      document.getElementById('customRestaurantInput').value = '';
    } else if (currentFun) {
      currentFun = null;
      document.querySelectorAll('.fun-card').forEach(c => c.classList.remove('active'));
      document.getElementById('funDetails').innerHTML = '';
    } else if (currentLocation) {
      currentLocation = null;
      document.querySelectorAll('.location-card').forEach(c => c.classList.remove('active'));
      document.getElementById('locationDetails').innerHTML = '';
      document.getElementById('restaurantSection').style.display = 'none';
      document.getElementById('dishesSection').style.display = 'none';
    } else if (currentWalk) {
      currentWalk = null;
      document.querySelectorAll('.walk-card').forEach(c => c.classList.remove('active'));
      document.getElementById('walkDetails').innerHTML = '';
    } else if (currentActivity) {
      currentActivity = null;
      document.querySelectorAll('.activity-card').forEach(c => c.classList.remove('active'));
      document.getElementById('activityDetails').innerHTML = '';
      document.getElementById('locationSection').style.display = 'none';
      document.getElementById('restaurantSection').style.display = 'none';
      document.getElementById('walkSection').style.display = 'none';
      document.getElementById('funSection').style.display = 'none';
      document.getElementById('dishesSection').style.display = 'none';
    }
  }

  renderDay('mon');

  const hearts = ['💙', '🩵', '🫧', '💎', '🐾', '🌊'];
  function createHeart() {
    const heart = document.createElement('div');
    heart.className = 'heart';
    heart.textContent = hearts[Math.floor(Math.random() * hearts.length)];
    heart.style.left = Math.random() * 100 + 'vw';
    heart.style.animationDuration = (Math.random() * 3 + 4) + 's';
    heart.style.fontSize = (Math.random() * 20 + 15) + 'px';
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 7000);
  }
  setInterval(createHeart, 500);

  function runAway() {
    const btn = document.getElementById('noBtn');
    const maxX = window.innerWidth - btn.offsetWidth - 20;
    const maxY = window.innerHeight - btn.offsetHeight - 20;
    btn.style.position = 'fixed';
    btn.style.left = Math.random() * maxX + 'px';
    btn.style.top = Math.random() * maxY + 'px';
    btn.textContent = ['Саша, ну пожааалуйста 😅', 'Ты точно? 🥺', 'Подумай ещё 💭', 'Серьёзно? 😢', 'Александра, не надо 🙏'][Math.floor(Math.random() * 5)];
  }

  function escapeHtml(text) {
    const div = document.createElement('div');
    div.textContent = text;
    return div.innerHTML;
  }

  async function sendToGoogleSheets(data) {
    if (!GOOGLE_SCRIPT_URL || GOOGLE_SCRIPT_URL.includes('ВСТАВЬ_СЮДА')) {
      console.warn('Google Script URL не настроен');
      return { success: false, error: 'URL не настроен' };
    }
    try {
      await fetch(GOOGLE_SCRIPT_URL, {
        method: 'POST',
        mode: 'no-cors',
        headers: { 'Content-Type': 'text/plain;charset=utf-8' },
        body: JSON.stringify(data)
      });
      return { success: true };
    } catch (error) {
      console.error('Ошибка отправки:', error);
      return { success: false, error: error.message };
    }
  }

  async function sayYes() {
    if (!currentActivity) {
      alert('Выбери, чем займёмся 😉');
      document.getElementById('activitySection').scrollIntoView({ behavior: 'smooth' }); return;
    }
    if (currentActivity === 'dinner' && !currentLocation) {
      alert('Выбери, где поужинаем 😉');
      document.getElementById('locationSection').scrollIntoView({ behavior: 'smooth' }); return;
    }
    if (currentActivity === 'dinner' && currentLocation === 'restaurant' && !currentRestaurant) {
      alert('Выбери ресторан 😉');
      document.getElementById('restaurantSection').scrollIntoView({ behavior: 'smooth' }); return;
    }
    if (currentActivity === 'dinner' && currentLocation === 'restaurant' && currentRestaurant === 'custom' && !customRestaurantName) {
      alert('Напиши название своего варианта ресторана 😉');
      document.getElementById('customRestaurantInput').focus(); return;
    }
    if (currentActivity === 'dinner' && currentLocation === 'home' && currentDishes.length === 0) {
      alert('Выбери хотя бы одно блюдо 😉');
      document.getElementById('dishesSection').scrollIntoView({ behavior: 'smooth' }); return;
    }
    if (currentActivity === 'walk' && !currentWalk) {
      alert('Выбери, куда пойдём гулять 😉');
      document.getElementById('walkSection').scrollIntoView({ behavior: 'smooth' }); return;
    }
    if (currentActivity === 'fun' && !currentFun) {
      alert('Выбери, куда пойдем развлекаться 😉');
      document.getElementById('funSection').scrollIntoView({ behavior: 'smooth' }); return;
    }
    
    const day = daysData[currentDay];
    const act = activitiesData[currentActivity];
    let finalDesc = act.desc, finalTime = act.time, finalName = act.name;
    let dishesHtml = '';
    
    const sheetData = {
      timestamp: new Date().toLocaleString('ru-RU'),
      name: 'Александра',
      day_key: currentDay,
      day_name: day.title,
      activity_key: currentActivity,
      activity_name: act.name,
      location_key: '',
      location_name: '',
      restaurant_key: '',
      restaurant_name: '',
      walk_key: '',
      walk_name: '',
      fun_key: '',
      fun_name: '',
      dishes: '',
      comment: document.getElementById('commentInput').value.trim()
    };
    
    if (currentActivity === 'dinner' && currentLocation) {
      const d = locationsData[currentLocation];
      finalDesc = d.desc; finalTime = d.time; finalName = `${act.name} ${d.name.toLowerCase()}`;
      sheetData.location_key = currentLocation;
      sheetData.location_name = d.name;
      
      if (currentLocation === 'restaurant' && currentRestaurant) {
        const r = restaurantData[currentRestaurant];
        const restName = currentRestaurant === 'custom' ? customRestaurantName : r.name;
        finalName = `${act.name} в ресторане "${restName}"`;
        sheetData.restaurant_key = currentRestaurant;
        sheetData.restaurant_name = restName;
      }
      
      if (currentLocation === 'home' && currentDishes.length > 0) {
        dishesHtml = '<p style="margin-top:12px;"><strong>🍽️ Меню:</strong></p><div>' +
          currentDishes.map(key => {
            const dd = dishesData[key];
            return `<span class="dish-tag">${dd.icon} ${dd.name}</span>`;
          }).join('') + '</div>';
        sheetData.dishes = currentDishes.map(key => dishesData[key].name).join(', ');
      }
    } else if (currentActivity === 'walk' && currentWalk) {
      const d = walkData[currentWalk]; finalDesc = d.desc; finalTime = d.time; finalName = d.name;
      sheetData.walk_key = currentWalk;
      sheetData.walk_name = d.name;
    } else if (currentActivity === 'fun' && currentFun) {
      const d = funData[currentFun]; finalDesc = d.desc; finalTime = d.time; finalName = d.name;
      sheetData.fun_key = currentFun;
      sheetData.fun_name = d.name;
    }
    
    const comment = document.getElementById('commentInput').value.trim();
    let commentHtml = '';
    if (comment) {
      commentHtml = `<div class="comment-block">${escapeHtml(comment)}</div>`;
    }
    
    const yesBtn = document.getElementById('yesBtn');
    const indicator = document.getElementById('sendingIndicator');
    yesBtn.disabled = true;
    indicator.classList.add('active');
    
    const sheetResult = await sendToGoogleSheets(sheetData);
    
    indicator.classList.remove('active');
    yesBtn.disabled = false;
    
    document.getElementById('mainCard').style.display = 'none';
    document.getElementById('successCard').style.display = 'block';
    document.getElementById('chosenInfo').innerHTML = `
      <p><strong>${day.icon} ${day.title}</strong> — ${day.desc}</p>
      <p><strong>${act.icon} ${finalName}</strong></p>
      <p>🕐 В ${finalTime}</p>
      <p style="margin-top:10px; font-style:italic;">${finalDesc}</p>
      ${dishesHtml}
      ${commentHtml}
    `;
    
    const statusDiv = document.getElementById('sheetStatus');
    if (sheetResult.success) {
      statusDiv.innerHTML = '<div class="sheet-status success">✅ Твой выбор сохранён и отправлен мне 💙</div>';
    } else {
      statusDiv.innerHTML = '<div class="sheet-status error">⚠️ Не удалось сохранить, но я всё равно всё запомню 💙</div>';
    }
    
    for (let i = 0; i < 60; i++) setTimeout(createHeart, i * 40);
  }
</script>

</body>
</html>
