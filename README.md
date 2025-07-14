<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Ranking ELO Güsak</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #121212;
      color: #FFFFFF;
      padding: 20px;
      margin: 0;
    }

    h1 {
      text-align: center;
      margin-bottom: 10px;
    }

    .tabs {
      display: flex;
      justify-content: center;
      margin-bottom: 30px;
    }

    .tab {
      padding: 10px 20px;
      margin: 0 5px;
      background-color: #2a2a2a;
      border: 1px solid #444;
      border-radius: 6px;
      color: #fff;
      cursor: pointer;
      font-weight: bold;
    }

    .tab.active {
      background-color: #444;
      color: #00ffc3;
    }

    .ranking {
      display: none;
      max-width: 500px;
      margin: 0 auto;
      background-color: #1e1e1e;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    .ranking.active {
      display: block;
    }

    h2 {
      text-align: center;
      margin-bottom: 20px;
    }

    table {
      width: 100%;
      border-collapse: collapse;
    }

    td {
      padding: 12px;
      border-bottom: 1px solid #333;
    }

    td.name {
      text-align: left;
      color: #000000;
    }

    td.points {
      text-align: center;
      font-weight: bold;
      color: #00ffc3;
    }
  </style>
</head>
<body>
  <h1>Ranking ELO Güsak 🪱</h1>

  <div class="tabs">
    <div class="tab active" onclick="showRanking('futbol', this)">⚽️ Fútbol</div>
    <div class="tab" onclick="showRanking('mus', this)">🃏 Mus</div>
  </div>

  <div id="futbol" class="ranking active">
    <h2>⚽️ Fútbol</h2>
    <table>
      <tbody>
        <tr><td class="name">Markel</td><td class="points">1438</td></tr>
        <tr><td class="name">Galder</td><td class="points">1377</td></tr>
        <tr><td class="name">Aimar</td><td class="points">1372</td></tr>
        <tr><td class="name">Ruiz</td><td class="points">1372</td></tr>
        <tr><td class="name">Carre</td><td class="points">1307</td></tr>
        <tr><td class="name">Ander</td><td class="points">1269</td></tr>
        <tr><td class="name">Rio</td><td class="points">1227</td></tr>
        <tr><td class="name">Danel</td><td class="points">1193</td></tr>
        <tr><td class="name">Bilbao</td><td class="points">1173</td></tr>
        <tr><td class="name">Salva</td><td class="points">1149</td></tr>
        <tr><td class="name">Garay</td><td class="points">1131</td></tr>
        <tr><td class="name">Ima</td><td class="points">1093</td></tr>
        <tr><td class="name">Josu</td><td class="points">964</td></tr>
        <tr><td class="name">Almi</td><td class="points">920</td></tr>
        <tr><td class="name">Ibon</td><td class="points">920</td></tr>
      </tbody>
    </table>
  </div>

  <div id="mus" class="ranking">
    <h2>🃏 Mus</h2>
    <table>
      <tbody>
        <tr><td class="name">Garay</td><td class="points">1444</td></tr>
        <tr><td class="name">Josu</td><td class="points">1402</td></tr>
        <tr><td class="name">Rodri</td><td class="points">1334</td></tr>
        <tr><td class="name">Enaitz</td><td class="points">1207</td></tr>
        <tr><td class="name">Ander</td><td class="points">1179</td></tr>
        <tr><td class="name">Salva</td><td class="points">1149</td></tr>
        <tr><td class="name">Lander</td><td class="points">1147</td></tr>
        <tr><td class="name">Danel</td><td class="points">1145</td></tr>
        <tr><td class="name">Rio</td><td class="points">1130</td></tr>
        <tr><td class="name">Carre</td><td class="points">1099</td></tr>
      </tbody>
    </table>
  </div>

  <script>
    function showRanking(id, tabElement) {
      const rankings = document.querySelectorAll('.ranking');
      const tabs = document.querySelectorAll('.tab');

      rankings.forEach(r => r.classList.remove('active'));
      tabs.forEach(t => t.classList.remove('active'));

      document.getElementById(id).classList.add('active');
      tabElement.classList.add('active');
    }
  </script>
</body>
</html>
