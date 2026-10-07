<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Solar Quality and PSI Dashboard</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f6fa;
      color: #1f2937;
    }

    header {
      background: linear-gradient(135deg, #123c69, #087f8c);
      color: white;
      padding: 32px 18px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 28px;
    }

    header p {
      margin: 10px 0 0;
    }

    .container {
      max-width: 1150px;
      margin: auto;
      padding: 20px 15px;
    }

    .profile {
      background: white;
      padding: 18px;
      border-radius: 12px;
      margin-bottom: 20px;
      box-shadow: 0 3px 10px #d7dce3;
    }

    .profile h2 {
      color: #123c69;
      margin-top: 0;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
      gap: 15px;
    }

    .card {
      background: white;
      padding: 18px;
      border-radius: 12px;
      box-shadow: 0 3px 10px #d7dce3;
      text-align: center;
    }

    .card h3 {
      color: #123c69;
      margin-top: 0;
    }

    .value {
      font-size: 26px;
      font-weight: bold;
      color: #087f8c;
    }

    .label {
      color: #6b7280;
      margin-top: 5px;
    }

    .status {
      display: inline-block;
      padding: 7px 13px;
      border-radius: 20px;
      font-weight: bold;
    }

    .running {
      background: #dcfce7;
      color: #166534;
    }

    .monitoring {
      background: #fef3c7;
      color: #92400e;
    }

    .section-title {
      margin-top: 28px;
      color: #123c69;
    }

    .panel {
      background: white;
      padding: 20px;
      margin-top: 20px;
      border-radius: 12px;
      box-shadow: 0 3px 10px #d7dce3;
    }

    .checklist {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .checklist li {
      padding: 12px 5px;
      border-bottom: 1px solid #e5e7eb;
    }

    .checklist input {
      margin-right: 10px;
      transform: scale(1.2);
    }

    .note {
      background: #eff6ff;
      border-left: 5px solid #2563eb;
      padding: 14px;
      margin-top: 20px;
      border-radius: 6px;
    }

    button {
      background: #123c69;
      color: white;
      border: none;
      padding: 12px 18px;
      border-radius: 6px;
      cursor: pointer;
      margin-top: 15px;
    }

    button:hover {
      background: #087f8c;
    }

    footer {
      background: #123c69;
      color: white;
      text-align: center;
      padding: 18px;
      margin-top: 30px;
    }
  </style>
</head>

<body>

  <header>
    <h1>Solar Quality and PSI Dashboard</h1>
    <p>Production, Inspection and Quality Monitoring</p>
  </header>

  <div class="container">

    <div class="profile">
      <h2>Current Responsibility</h2>
      <p><strong>Name:</strong> Nikunj</p>
      <p><strong>Current Role:</strong> PSI</p>
      <p>
        <strong>Line Leader Experience:</strong>
        POST EL, LAM EL, Sun Simulator, FQC, VQC and Backend
      </p>
      <p><strong>Shift Status:</strong> <span class="status running">Active</span></p>
    </div>

    <h2 class="section-title">Process Area Status</h2>

    <div class="cards">

      <div class="card">
        <h3>POST EL</h3>
        <div class="value">Ready</div>
        <div class="label">Post-lamination EL Inspection</div>
        <p><span class="status running">Monitoring</span></p>
      </div>

      <div class="card">
        <h3>LAM EL</h3>
        <div class="value">Ready</div>
        <div class="label">Lamination EL Inspection</div>
        <p><span class="status running">Monitoring</span></p>
      </div>

      <div class="card">
        <h3>Sun Simulator</h3>
        <div class="value">Ready</div>
        <div class="label">Power and IV Test</div>
        <p><span class="status running">Monitoring</span></p>
      </div>

      <div class="card">
        <h3>FQC</h3>
        <div class="value">Active</div>
        <div class="label">Final Quality Control</div>
        <p><span class="status running">Running</span></p>
      </div>

      <div class="card">
        <h3>VQC</h3>
        <div class="value">Active</div>
        <div class="label">Visual Quality Control</div>
        <p><span class="status running">Running</span></p>
      </div>

      <div class="card">
        <h3>Backend</h3>
        <div class="value">Active</div>
        <div class="label">Backend Process Area</div>
        <p><span class="status running">Running</span></p>
      </div>

    </div>

    <h2 class="section-title">Daily PSI Checklist</h2>

    <div class="panel">
      <ul class="checklist">

        <li>
          <label>
            <input type="checkbox">
            Confirm shift handover and production target
          </label>
        </li>

        <li>
          <label>
            <input type="checkbox">
            Check POST EL and LAM EL inspection status
          </label>
        </li>

        <li>
          <label>
            <input type="checkbox">
            Verify Sun Simulator test records
          </label>
        </li>

        <li>
          <label>
            <input type="checkbox">
            Review FQC and VQC quality observations
          </label>
        </li>

        <li>
          <label>
            <input type="checkbox">
            Check backend line output and pending issues
          </label>
        </li>

        <li>
          <label>
            <input type="checkbox">
            Record defects, rework and rejection details
          </label>
        </li>

        <li>
          <label>
            <input type="checkbox">
            Complete shift report and handover
          </label>
        </li>

      </ul>

      <button onclick="checkProgress()">Check Checklist Progress</button>
      <p id="progressMessage"></p>
    </div>

    <div class="note">
      <strong>Important:</strong>
      This is a personal demo dashboard. Do not enter confidential company data,
      product serial numbers, customer information or restricted process details.
      Always follow your company's approved SOP and quality procedures.
    </div>

  </div>

  <footer>
    <p>Solar Quality and PSI Dashboard | Created by Nikunj</p>
  </footer>

  <script>
    function checkProgress() {
      const tasks = document.querySelectorAll(
        '.checklist input[type="checkbox"]'
      );

      let completed = 0;

      tasks.forEach(function(task) {
        if (task.checked) {
          completed++;
        }
      });

      document.getElementById("progressMessage").innerText =
        completed + " of " + tasks.length + " tasks completed.";
    }
  </script>

</body>
</html>