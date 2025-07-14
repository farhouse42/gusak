<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Ranking ELO - Güsak</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #121212;
      color: #f0f0f0;
      padding: 20px;
    }
    h1 {
      text-align: center;
    }
    .tabs {
      display: flex;
      justify-content: center;
      margin-top: 30px;
    }
    .tab {
      padding: 10px 20px;
      background: #1e1e1e;
      border: 1px solid #333;
      cursor: pointer;
      margin: 0 5px;
      border-radius: 6px 6px 0 0;
      font-weight: bold;
    }
    .tab.active {
      background: #333;
    }
    .ranking {
      max-width: 500px;
      margin: 0 auto;
      background: #1e1e1e;
      border-radius: 0 0 10px 10px;
      padding: 20px;
      box-shadow: 0 0 10px rgba(255,255,255,0.1);
      display: none;
    }
    .ranking.active {
      display: block;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 10px;
    }
    th, td {
      padding: 10px;
      border-bottom: 1px solid #333;
    }
    td.name {
      text-align: left;
    }
    td.points {
      text-align: center;
      font-family: 'Consolas', monospace;
      font-size: 1.1em;
      color: #00ffcc;
    }
  </style>
</head>
<body>
  <h1>Ranking ELO Güsak 🪱</h1>

  <div class="tabs">
    <div class="tab active" onclick="showRanking('futbol')">⚽️ Fútbol</div>
    <div class="tab" onclick="showRanking('mus')">🃏 Mus</div>
  </div>

  <div id="futbol" class="ranking active">
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
    function showRanking(id) {
      const tabs = document.querySelectorAll('.tab');
      const rankings = document.querySelectorAll('.ranking');
      tabs.forEach(tab => tab.classList.remove('active'));
      rankings.forEach(ranking => ranking.classList.remove('active'));
      document.getElementById(id).classList.add('active');
      event.target.classList.add('active');
    }
  </script>
</body>
</html>
