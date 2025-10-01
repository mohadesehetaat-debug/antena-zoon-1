
<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <title>نقشه شبکه پارک نهج البلاغه - فاز ۱</title>
  <style>
    body {
      font-family: sans-serif;
      direction: rtl;
      background: #f4f6f8;
      margin: 0;
      padding: 20px;
    }
    h1 { text-align: center; margin-bottom: 20px; }

    .diagram {
      position: relative;
      max-width: 1000px;
      height: 600px;
      margin: 0 auto;
      background: #fff;
      border: 1px solid #ccc;
      border-radius: 12px;
      padding: 20px;
    }

    .node {
      position: absolute;
      width: 140px;
      padding: 6px;
      border: 2px solid #339af0;
      border-radius: 8px;
      background: #e7f3ff;
      font-size: 12px;
      text-align: center;
      cursor: pointer;
    }
    .title { font-weight: bold; margin-bottom: 4px; }
    .icon { font-size: 14px; }

    /* منوی کشویی */
    .panel {
      max-height: 0;
      overflow: hidden;
      transition: max-height 0.3s ease;
      background: #fff;
      border: 1px dashed #339af0;
      border-radius: 6px;
      margin-top: 6px;
      padding: 0 6px;
      font-size: 11px;
    }
    .panel.open {
      max-height: 200px;
      padding: 6px;
    }
    .panel p { margin: 4px 0; }
    .panel a { font-size: 11px; color: #007bff; text-decoration: none; }

    /* موقعیت‌ها */
    #AP1GM { bottom: 40px; left: 40px; }
    #AP3GMT { top: 60px; left: 200px; }
    #AP4HTO { top: 60px; left: 400px; }
    #AP5HO { top: 60px; left: 600px; }

    #AP3H { bottom: 60px; left: 200px; }
    #AP6HO1 { bottom: 60px; left: 400px; }
    #AP7ZE { bottom: 60px; left: 600px; }
  </style>
</head>
<body>
  <h1>📡 نقشه شبکه پارک نهج البلاغه - فاز ۱</h1>
  <div class="diagram">
    <!-- کانکس شهرداری -->
    <div class="node" id="AP1GM" onclick="togglePanel('p1')">
      <div class="title"><span class="icon">🏠</span> AP1GM</div>
      <div class="panel" id="p1">
        <p><b>TX:</b> ارسال به AP3GMT</p>
        <p><b>توضیح:</b> تغذیه اولیه شبکه</p>
        <a href="https://www.google.com/maps?q=35.7295,51.3120" target="_blank">📍 Google Maps</a><br>
        <a href="https://earth.google.com/web/search/35.7295,51.3120" target="_blank">🌍 Google Earth</a>
      </div>
    </div>

    <!-- دکل همیلا ۱ -->
    <div class="node" id="AP3GMT" onclick="togglePanel('p2')">
      <div class="title"><span class="icon">📡</span> AP3GMT</div>
      <div class="panel" id="p2">
        <p><b>RX:</b> از AP1GM</p>
        <p><b>TX:</b> به AP4HTO و AP5HO</p>
        <a href="https://www.google.com/maps?q=35.7312,51.3145" target="_blank">📍 Google Maps</a><br>
        <a href="https://earth.google.com/web/search/35.7312,51.3145" target="_blank">🌍 Google Earth</a>
      </div>
    </div>

    <!-- آنتن PTP -->
    <div class="node" id="AP4HTO" onclick="togglePanel('p3')">
      <div class="title"><span class="icon">📶</span> AP4HTO</div>
      <div class="panel" id="p3">
        <p><b>TX:</b> به AP3H</p>
        <p><b>RX:</b> از AP3GMT</p>
        <a href="https://www.google.com/maps?q=35.7300,51.3130" target="_blank">📍 Google Maps</a><br>
        <a href="https://earth.google.com/web/search/35.7300,51.3130" target="_blank">🌍 Google Earth</a>
      </div>
    </div>

    <!-- آنتن PTP -->
    <div class="node" id="AP5HO" onclick="togglePanel('p4')">
      <div class="title"><span class="icon">📶</span> AP5HO</div>
      <div class="panel" id="p4">
        <p><b>TX:</b> به AP6HO1</p>
        <p><b>RX:</b> از AP3GMT</p>
        <a href="https://www.google.com/maps?q=35.7305,51.3135" target="_blank">📍 Google Maps</a><br>
        <a href="https://earth.google.com/web/search/35.7305,51.3135" target="_blank">🌍 Google Earth</a>
      </div>
    </div>

    <!-- دکل ایوانک -->
    <div class="node" id="AP3H" onclick="togglePanel('p5')">
      <div class="title"><span class="icon">📡</span> AP3H</div>
      <div class="panel" id="p5">
        <p><b>RX:</b> از AP4HTO</p>
        <a href="https://www.google.com/maps?q=35.7280,51.3110" target="_blank">📍 Google Maps</a><br>
        <a href="https://earth.google.com/web/search/35.7280,51.3110" target="_blank">🌍 Google Earth</a>
      </div>
    </div>

    <!-- دکل همیلا ۳ -->
    <div class="node" id="AP6HO1" onclick="togglePanel('p6')">
      <div class="title"><span class="icon">📡</span> AP6HO1</div>
      <div class="panel" id="p6">
        <p><b>RX:</b> از AP5HO</p>
        <p><b>TX:</b> به AP7ZE</p>
        <a href="https://www.google.com/maps?q=35.7275,51.3140" target="_blank">📍 Google Maps</a><br>
        <a href="https://earth.google.com/web/search/35.7275,51.3140" target="_blank">🌍 Google Earth</a>
      </div>
    </div>

    <!-- دکل همیلا ۲ -->
    <div class="node" id="AP7ZE" onclick="togglePanel('p7')">
      <div class="title"><span class="icon">📡</span> AP7ZE</div>
      <div class="panel" id="p7">
        <p><b>RX:</b> از AP6HO1</p>
        <a href="https://www.google.com/maps?q=35.7265,51.3145" target="_blank">📍 Google Maps</a><br>
        <a href="https://earth.google.com/web/search/35.7265,51.3145" target="_blank">🌍 Google Earth</a>
      </div>
    </div>
  </div>

  <script>
    function togglePanel(id) {
      document.querySelectorAll('.panel').forEach(p => p.classList.remove('open'));
      const el = document.getElementById(id);
      el.classList.add('open');
    }
  </script>
</body>
</html>
<!-- بخش توضیحات به صورت جدول -->
<div class="legend">
  <h3>راهنمای نمادها</h3>
  <table>
    <tr>
      <td>🏠</td>
      <td>کانکس شهرداری (مبدأ شبکه)</td>
    </tr>
    <tr>
      <td>📡</td>
      <td>دکل اصلی / ایستگاه پایه</td>
    </tr>
    <tr>
      <td>📶</td>
      <td>آنتن PTP (ارتباط نقطه به نقطه)</td>
    </tr>
    <tr>
      <td><b>TX</b></td>
      <td>فرستنده (انتقال داده)</td>
    </tr>
    <tr>
      <td><b>RX</b></td>
      <td>گیرنده (دریافت داده)</td>
    </tr>
  </table>
</div>

<style>
  .legend {
    max-width: 400px;
    margin: 15px auto;
    background: #fff;
    border: 1px solid #ccc;
    border-radius: 6px;
    padding: 8px;
    font-size: 12px;
  }
  .legend h3 {
    margin: 0 0 6px 0;
    font-size: 13px;
    text-align: center;
    color: #333;
  }
  .legend table {
    width: 100%;
    border-collapse: collapse;
  }
  .legend td {
    padding: 4px 6px;
    border-bottom: 1px solid #eee;
  }
  .legend tr:last-child td {
    border-bottom: none;
  }
  .legend td:first-child {
    width: 40px;
    text-align: center;
  }
</style>
