<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Ranking ELO Güsak</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: #f0f0f0;
      margin: 0;
      padding: 20px;
    }

    h1 {
      text-align: center;
      margin-bottom: 20px;
      font-size: 2.2em;
    }

    .tabs {
      display: flex;
      justify-content: center;
      margin-bottom: 30px;
    }

    .tab {
      padding: 10px 20px;
      margin: 0 8px;
      background-color: #1e1e1e;
      border: none;
      border-radius: 8px;
      color: #ccc;
      cursor: pointer;
      font-weight: 600;
      transition: all 0.3s ease;
    }

    .tab:hover {
      background-color: #2a2a2a;
      color: #fff;
    }

    .tab.active {
      background-color: #00ffc3;
      color: #121212;
    }

    .ranking {
      display: none;
      max-width: 500px;
      margin: 0 auto;
      background: rgba(30, 30, 30, 0.8);
      border-radius: 12px;
      padding: 20px;
      backdrop-filter: blur(10px);
      box-shadow: 0 8px 20px rgba(0,0,0,0.4);
      opacity: 0;
      transform: translateY(20px);
      transition: all 0.4s ease;
    }

    .ranking.active {
      display: block;
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      text-align: center;
      margin-bottom: 15px;
      color: #00ffc3;
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
    }

    td.points {
      text-align: right;
      font-weight: bold;
      color: #00ffc3;
    }

    /* Resaltar líder */
    tbody tr:first-child td.name {
      color: gold;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Ranking ELO Güsak 🐍</h1>

  <div class="tabs">
    <button class="tab active" onclick="showRanking('futbol', this)">⚽ Fútbol</button>
    <button class="tab" onclick="showRanking('mus', this)">🃏 Mus</button>
  </div>

  <div id="futbol" class="ranking active">
    <h2>⚽ Fútbol</h2>
    <table>
      <tbody>
        <tr><td class="name">Markel 🏆</td><td class="points">1438</td></tr>
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
        <tr><td class="name">Garay 🏆</td><td class="points">1444</td></tr>
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
