<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>LUCENT COACHING CENTRE - Bill Book System</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700;900&display=swap" rel="stylesheet">
  
  <!-- CSS STYLING -->
  <style>
    :root {
      --primary-black: #000000;
      --navy-blue: #002244;
      --bg-slate: #cbd5e1;
      --card-bg: #ffffff;
      --border-dark: #334155;
      --danger-red: #b91c1c;
      --success-green: #15803d;
      --phonepe-purple: #6b21a8;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Roboto', sans-serif;
    }

    body {
      background-color: var(--bg-slate);
      color: #0f172a;
      padding: 25px 12px;
    }

    /* MAIN RECTANGULAR CARD */
    .bill-wrapper {
      max-width: 740px;
      margin: 0 auto;
      background: var(--card-bg);
      border: 3px solid var(--primary-black);
      border-radius: 0px;
      box-shadow: 8px 8px 0px rgba(0, 0, 0, 0.85);
    }

    /* HEADER */
    .bill-header {
      background: var(--card-bg);
      padding: 24px 18px 18px;
      text-align: center;
      border-bottom: 3px solid var(--primary-black);
    }

    /* 36PX TIMES NEW ROMAN BLACK BOLD */
    .bill-header h1 {
      font-family: 'Times New Roman', Times, serif !important;
      font-size: 36px !important;
      font-weight: 900 !important;
      color: var(--primary-black) !important;
      letter-spacing: 0.5px;
      line-height: 1.15;
      text-transform: uppercase;
      margin-bottom: 6px;
    }

    .bill-header .inst-sub {
      font-family: 'Times New Roman', Times, serif;
      font-size: 15px;
      font-weight: 700;
      color: #1e293b;
      margin-bottom: 4px;
    }

    .bill-header .inst-phone {
      font-family: 'Times New Roman', Times, serif;
      font-size: 15px;
      font-weight: 700;
      color: #0f172a;
      margin-bottom: 10px;
    }

    .leader-row {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 6px;
    }

    .leader-badge {
      background: #f1f5f9;
      border: 1.5px solid #0f172a;
      padding: 4px 12px;
      font-size: 12px;
      font-weight: 800;
      color: #0f172a;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .badge-sub {
      background: var(--navy-blue);
      color: #ffffff;
      font-size: 11.5px;
      font-weight: 800;
      padding: 5px 14px;
      display: inline-block;
      margin-top: 10px;
      letter-spacing: 0.5px;
      text-transform: uppercase;
    }

    /* FORM BODY */
    .bill-body {
      padding: 22px;
    }

    .grid-2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 14px;
      margin-bottom: 14px;
    }

    .grid-3 {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 12px;
      margin-bottom: 14px;
    }

    .field-box {
      display: flex;
      flex-direction: column;
    }

    .field-box label {
      font-size: 12px;
      font-weight: 800;
      color: #1e293b;
      margin-bottom: 5px;
      text-transform: uppercase;
    }

    .field-box input,
    .field-box select {
      width: 100%;
      padding: 10px 12px;
      font-size: 14px;
      border: 2px solid var(--border-dark);
      border-radius: 0px;
      background: #ffffff;
      color: #0f172a;
      outline: none;
      font-weight: 600;
      transition: all 0.2s ease;
    }

    .field-box input:focus,
    .field-box select:focus {
      border-color: #0284c7;
      background: #f0f9ff;
    }

    .month-select-lg {
      padding: 11px 12px !important;
      font-size: 15px !important;
      font-weight: 800 !important;
      color: var(--primary-black) !important;
      border: 2px solid var(--primary-black) !important;
      background: #f8fafc !important;
      cursor: pointer;
    }

    /* REALTIME CALCULATION BAR */
    .math-bar {
      background: #f8fafc;
      border: 2px solid var(--primary-black);
      border-radius: 0px;
      padding: 14px;
      margin: 16px 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 10px;
    }

    .math-bar .math-desc {
      font-size: 12.5px;
      color: #334155;
      font-weight: 700;
    }

    .math-bar .math-total {
      text-align: right;
    }

    .math-bar .math-total span {
      font-size: 11px;
      font-weight: 800;
      color: var(--navy-blue);
      display: block;
      text-transform: uppercase;
    }

    .math-bar .math-total strong {
      font-size: 24px;
      color: var(--danger-red);
      font-weight: 900;
    }

    /* PHONEPE PAYMENT & QR CARD */
    .qr-payment-card {
      background: #faf5ff;
      border: 2px dashed #9333ea;
      border-radius: 0px;
      padding: 14px;
      margin-bottom: 16px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 12px;
    }

    .qr-info-text {
      font-size: 13px;
      color: #3b0764;
      line-height: 1.6;
    }

    .qr-info-text strong {
      color: #581c87;
    }

    .qr-box-img {
      text-align: center;
      background: #ffffff;
      padding: 6px;
      border: 1.5px solid #c084fc;
      border-radius: 0px;
    }

    .qr-box-img img {
      width: 110px;
      height: 110px;
      display: block;
      object-fit: contain;
    }

    .qr-box-img span {
      font-size: 9px;
      font-weight: 800;
      color: var(--phonepe-purple);
      display: block;
      margin-top: 2px;
    }

    /* PREVIEW CONTAINER */
    .preview-area {
      background: #f8fafc;
      border: 2px solid #94a3b8;
      border-radius: 0px;
      padding: 12px;
      font-size: 12.5px;
      line-height: 1.6;
      color: #1e293b;
      white-space: pre-wrap;
      margin-bottom: 18px;
      max-height: 180px;
      overflow-y: auto;
    }

    /* ACTION BUTTONS */
    .action-btn-row {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 10px;
    }

    .btn-custom {
      width: 100%;
      border-radius: 0px;
      padding: 13px 8px;
      font-size: 13px;
      font-weight: 900;
      cursor: pointer;
      text-transform: uppercase;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
      transition: all 0.1s ease;
    }

    .btn-custom-print {
      background: #0f172a;
      color: #ffffff;
      border: 2px solid var(--primary-black);
      box-shadow: 4px 4px 0px var(--primary-black);
    }
    .btn-custom-print:hover {
      background: #1e293b;
      transform: translate(1px, 1px);
      box-shadow: 3px 3px 0px var(--primary-black);
    }

    .btn-custom-wa {
      background: #16a34a;
      color: #ffffff;
      border: 2px solid #14532d;
      box-shadow: 4px 4px 0px #14532d;
    }
    .btn-custom-wa:hover {
      background: var(--success-green);
      transform: translate(1px, 1px);
      box-shadow: 3px 3px 0px #14532d;
    }

    .btn-custom-sms {
      background: #0284c7;
      color: #ffffff;
      border: 2px solid #0369a1;
      box-shadow: 4px 4px 0px #0369a1;
    }
    .btn-custom-sms:hover {
      background: #0369a1;
      transform: translate(1px, 1px);
      box-shadow: 3px 3px 0px #0369a1;
    }

    .btn-custom:active {
      transform: translate(3px, 3px);
      box-shadow: none;
    }

    /* PRINT / PDF STYLING */
    #printInvoiceArea {
      display: none;
    }

    @media print {
      body * {
        visibility: hidden;
      }
      #printInvoiceArea, #printInvoiceArea * {
        visibility: visible;
      }
      #printInvoiceArea {
        display: block !important;
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        padding: 20px;
        background: #ffffff;
        color: #000000;
      }
      .paper-invoice {
        border: 2.5px solid #000000;
        padding: 20px;
        max-width: 620px;
        margin: 0 auto;
      }
      .pi-head {
        text-align: center;
        border-bottom: 2px solid #000000;
        padding-bottom: 10px;
        margin-bottom: 12px;
      }
      .pi-head h2 {
        font-family: 'Times New Roman', Times, serif;
        font-size: 28px;
        text-transform: uppercase;
        font-weight: 900;
        margin-bottom: 4px;
      }
      .pi-head p {
        font-family: 'Times New Roman', Times, serif;
        font-size: 13px;
        font-weight: 600;
        line-height: 1.4;
      }
      .pi-leaders {
        font-size: 11px;
        font-weight: bold;
        margin-top: 5px;
        text-transform: uppercase;
      }
      .pi-meta {
        display: flex;
        justify-content: space-between;
        font-size: 13px;
        font-weight: bold;
        margin-bottom: 12px;
        border-bottom: 1px dashed #000000;
        padding-bottom: 6px;
      }
      .pi-table {
        width: 100%;
        border-collapse: collapse;
        margin-bottom: 12px;
      }
      .pi-table th, .pi-table td {
        border: 1px solid #000000;
        padding: 8px 10px;
        font-size: 13px;
        text-align: left;
      }
      .pi-table th {
        background: #f8fafc;
        width: 42%;
      }
      .pi-footer {
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        margin-top: 35px;
      }
      .pi-sign {
        border-top: 1.5px solid #000000;
        width: 170px;
        text-align: center;
        font-size: 11.5px;
        font-weight: bold;
      }
    }

    @media (max-width: 650px) {
      .bill-header h1 {
        font-size: 28px !important;
      }
      .grid-2, .grid-3, .action-btn-row {
        grid-template-columns: 1fr;
      }
      .math-bar {
        flex-direction: column;
        align-items: flex-start;
      }
      .math-bar .math-total {
        text-align: left;
      }
      .qr-payment-card {
        flex-direction: column;
        align-items: flex-start;
      }
    }
  </style>
</head>
<body>

  <!-- BILL BOOK HTML WRAPPER -->
  <div class="bill-wrapper">
    <div class="bill-header">
      <h1>LUCENT COACHING CENTRE</h1>
      <div class="inst-sub">Near Mithila Eye Hospital, Musrigharari, Samastipur (Bihar) - 848211[span_3](start_span)[span_3](end_span)</div>
      <div class="inst-phone">Contact / Helpline: <strong>+91 8789524958</strong>[span_4](start_span)[span_4](end_span)</div>
      <div class="leader-row">
        <div class="leader-badge">Director: <strong>Md Mahfooz Alam</strong>[span_5](start_span)[span_5](end_span)</div>
        <div class="leader-badge">Managing Director: <strong>Md Nazir</strong></div>
      </div>
      <div>
        <div class="badge-sub">★ OFFICIAL STUDENT FEE BILL BOOK ★</div>
      </div>
    </div>

    <div class="bill-body">
      <!-- Row 1: Student Selection -->
      <div class="grid-2">
        <div class="field-box">
          <label>छात्र चुनें (Dropdown List) *</label>
          <select id="studentSelect" onchange="onStudentSelectChange()">
            <option value="">-- छात्र का नाम चुनें --</option>
          </select>
        </div>
        <div class="field-box">
          <label>Student Full Name:</label>
          <input type="text" id="studentName" placeholder="उदा. Rahul Kumar" oninput="calculateBill()">
        </div>
      </div>

      <!-- Row 2: Phone & Class -->
      <div class="grid-2">
        <div class="field-box">
          <label>Parents Mobile Number *</label>
          <input type="tel" id="parentPhone" placeholder="10 अंकों का मोबाइल नंबर">
        </div>
        <div class="field-box">
          <label>Class / Course *</label>
          <input type="text" id="studentClass" value="12th" oninput="calculateBill()">
        </div>
      </div>

      <!-- Row 3: Month & Bill Date -->
      <div class="grid-2">
        <div class="field-box">
          <label>Fee Month (बिल का महीना) *</label>
          <select id="feeMonth" class="month-select-lg" onchange="calculateBill()">
            <option value="January 2026">January 2026</option>
            <option value="February 2026">February 2026</option>
            <option value="March 2026">March 2026</option>
            <option value="April 2026">April 2026</option>
            <option value="May 2026">May 2026</option>
            <option value="June 2026">June 2026</option>
            <option value="July 2026">July 2026</option>
            <option value="August 2026">August 2026</option>
            <option value="September 2026" selected>September 2026</option>
            <option value="October 2026">October 2026</option>
            <option value="November 2026">November 2026</option>
            <option value="December 2026">December 2026</option>
          </select>
        </div>
        <div class="field-box">
          <label>Bill Date (बिल जारी दिनांक) *</label>
          <input type="date" id="billDate" onchange="calculateBill()">
        </div>
      </div>

      <!-- Row 4: Math Calculations -->
      <div class="grid-3">
        <div class="field-box">
          <label>Previous Due (पिछला बकाया ₹):</label>
          <input type="number" id="prevDues" value="0" min="0" oninput="calculateBill()">
        </div>
        <div class="field-box">
          <label>Current Fee (चालू शुल्क ₹) *</label>
          <input type="number" id="currDues" value="450" min="0" oninput="calculateBill()">
        </div>
        <div class="field-box">
          <label>Discount / Paid (- ₹):</label>
          <input type="number" id="discountPaid" value="0" min="0" oninput="calculateBill()">
        </div>
      </div>

      <!-- Live Calculation Display -->
      <div class="math-bar">
        <div class="math-desc" id="mathBreakdown">
          विवरण: ₹0 (बकाया) + ₹450 (माह शुल्क) - ₹0 (छूट/अग्रिम)
        </div>
        <div class="math-total">
          <span>कुल देय बिल राशि (Total Bill Amount)</span>
          <strong id="totalPayableText">₹ 450</strong>
        </div>
      </div>

      <!-- PhonePe QR Code Component -->
      <div class="qr-payment-card">
        <div class="qr-info-text">
          <strong>🟣 PhonePe / UPI भुगतान विवरण:</strong><br>
          नाम: <b>Md Mahfooz</b>[span_6](start_span)[span_6](end_span)<br>
          PhonePe No: <b>8789524958</b>[span_7](start_span)[span_7](end_span)[span_8](start_span)[span_8](end_span)<br>
          UPI ID: <b>8789524958-2@ibl</b>[span_9](start_span)[span_9](end_span)
        </div>
        <div class="qr-box-img">
          <img src="1000187436.jpg" alt="PhonePe QR" onerror="this.src='https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=upi://pay?pa=8789524958-2@ibl%26pn=Md%20Mahfooz';">[span_10](start_span)[span_10](end_span)[span_11](start_span)[span_11](end_span)
          <span>SCAN TO PAY</span>
        </div>
      </div>

      <!-- Live Text Preview -->
      <label style="font-size: 11px; font-weight: 800; color: #475569; text-transform: uppercase; margin-bottom: 4px; display: block;">
        बिल मेसेज प्रीव्यू (WhatsApp / SMS):
      </label>
      <div class="preview-area" id="messagePreview"></div>

      <!-- Output Trigger Buttons -->
      <div class="action-btn-row">
        <button type="button" class="btn-custom btn-custom-print" onclick="printBillPDF()">
          <span>🖨️</span> प्रिंट / PDF बिल[span_12](start_span)[span_12](end_span)
        </button>
        <button type="button" class="btn-custom btn-custom-wa" onclick="sendBillMessage('whatsapp')">
          <span>💬</span> WhatsApp पर बिल[span_13](start_span)[span_13](end_span)
        </button>
        <button type="button" class="btn-custom btn-custom-sms" onclick="sendBillMessage('sms')">
          <span>✉️</span> SMS पर बिल[span_14](start_span)[span_14](end_span)
        </button>
      </div>
    </div>
  </div>

  <!-- PRINT / PDF BILL TEMPLATE (HIDDEN ON SCREEN) -->
  <div id="printInvoiceArea">
    <div class="paper-invoice">
      <div class="pi-head">
        <h2>LUCENT COACHING CENTRE</h2>
        <p>Near Mithila Eye Hospital, Musrigharari, Samastipur (Bihar)[span_15](start_span)[span_15](end_span)</p>
        <p>Contact / Helpline: <strong>+91 8789524958</strong>[span_16](start_span)[span_16](end_span)</p>
        <div class="pi-leaders">
          Director: <strong>Md Mahfooz Alam</strong> | Managing Director: <strong>Md Nazir</strong>[span_17](start_span)[span_17](end_span)
        </div>
        <div style="font-weight: bold; margin-top: 6px; font-size: 13px; text-transform: uppercase;">
          ★ आधिकारिक शिक्षण शुल्क बिल (STUDENT FEE INVOICE) ★[span_18](start_span)[span_18](end_span)
        </div>
      </div>

      <div class="pi-meta">
        <div>बिल सं. (Bill No): <span id="billNo">LCC-BILL-101</span></div>
        <div>दिनांक (Date): <span id="billDateDisplay">26/09/2026</span></div>
      </div>

      <table class="pi-table">
        <tr>
          <th>विद्यार्थी का नाम:</th>
          <td id="bStudentName">Rahul Kumar</td>
        </tr>
        <tr>
          <th>कक्षा / बैच (Class):</th>
          <td id="bClass">12th</td>
        </tr>
        <tr>
          <th>अभिभावक संपर्क नंबर:</th>
          <td id="bPhone">9876543210</td>
        </tr>
        <tr>
          <th>बिल का महीना:</th>
          <td id="bMonth">September 2026</td>
        </tr>
        <tr>
          <th>पिछला बकाया शुल्क (Previous Due):</th>
          <td id="bPrevDue">₹0</td>
        </tr>
        <tr>
          <th>चालू माह शुल्क (Monthly Fee):</th>
          <td id="bCurrFee">₹450</td>
        </tr>
        <tr>
          <th>छूट / अग्रिम समायोजन:</th>
          <td id="bDiscount">₹0</td>
        </tr>
        <tr style="background: #f8fafc; font-weight: bold;">
          <th>कुल देय राशि (Total Amount Due):</th>
          <td id="bTotalPayable" style="font-size: 15px; color: #b91c1c;">₹450</td>
        </tr>
      </table>

      <div style="font-size: 11px; margin-top: 6px; color: #333;">
        * ऑनलाइन भुगतान: PhonePe No. <strong>8789524958</strong> (UPI: <strong>8789524958-2@ibl</strong>)[span_19](start_span)[span_19](end_span)
      </div>

      <div class="pi-footer">
        <div style="font-size: 11px;">Issued by: Lucent Office</div>
        <div class="pi-sign">प्राधिकृत हस्ताक्षर / मुहर</div>
      </div>
    </div>
  </div>

  <!-- JAVASCRIPT ENGINE -->
  <script>
    // Complete Verified Students Directory[span_20](start_span)[span_20](end_span)
    const studentsData = [
      { name: "AMJAD ALAM", phone: "9955684664" },
      { name: "ANAMIKA KRI", phone: "7257054499" },
      { name: "ANJALI KRI 25", phone: "9661935200" },
      { name: "Anjali Kumari 55", phone: "8102799207" },
      { name: "ANSHU KUMARI-9", phone: "7352082956" },
      { name: "Anshu kri-42", phone: "" },
      { name: "ANUPAM KRI", phone: "9241417455" },
      { name: "BEAUTY KUMARI", phone: "6200783994" },
      { name: "DHIRAJ KUMAR", phone: "6204035295" },
      { name: "DURGA KRI", phone: "9204523024" },
      { name: "GAUTAM KR", phone: "7352494184" },
      { name: "GOLU KR.", phone: "7654872555" },
      { name: "Jamila 12th", phone: "9341643733" },
      { name: "JASMIN PARWEEN", phone: "9693402311" },
      { name: "JULY KRI", phone: "8130457073" },
      { name: "KARINA KUMARI", phone: "7324983282" },
      { name: "KHUSHBOO KRI", phone: "7764836893" },
      { name: "Md Dilsan", phone: "9942833704" },
      { name: "MD MERAJ-17", phone: "9330773998" },
      { name: "MD MERAJ-41", phone: "7091859037" },
      { name: "MD SAJID", phone: "9204687474" },
      { name: "MD SIRAJ", phone: "7549898828" },
      { name: "MD WASIM", phone: "9102763861" },
      { name: "MEHAR KALI", phone: "6299956098" },
      { name: "MEHJABIN PARWEEN", phone: "9990688776" },
      { name: "MONIKA KRI", phone: "6201578087" },
      { name: "MUSARRAT PRAWEEN", phone: "7079910638" },
      { name: "MUSKAN BEGUM", phone: "9330942019" },
      { name: "NEHA KHATOON", phone: "9709587061" },
      { name: "NISHU KRI 30", phone: "8210975252" },
      { name: "NISHU KRI-45", phone: "8475868000" },
      { name: "PARITOSH KUMAR", phone: "9142869790" },
      { name: "PRITY KRI", phone: "7079598875" },
      { name: "PRIYANKA KRI", phone: "9155206202" },
      { name: "Priyanshu kr", phone: "7004128721" },
      { name: "RADHA KRI", phone: "9534005894" },
      { name: "RAGINI KRI", phone: "6201389319" },
      { name: "Raja kr", phone: "9296503161" },
      { name: "RAJ NANDINI KRI", phone: "8873126752" },
      { name: "RANJAN KUMAR", phone: "9709864426" },
      { name: "RAUSHNI KRI", phone: "9534758058" },
      { name: "RIMJHIM KRI", phone: "9570170325" },
      { name: "ROKHSANA KHATUN", phone: "9709658472" },
      { name: "RUPA KRI", phone: "9661273871" },
      { name: "SAHIN PARWEEN", phone: "7372035346" },
      { name: "SAMA AFREEN", phone: "9110989890" },
      { name: "SANDHNA KRI", phone: "8002000873" },
      { name: "SANIYA PARWEEN", phone: "7654162435" },
      { name: "SAVITA KRI", phone: "7544842569" },
      { name: "SHAHNAWAZ HUSSAIN", phone: "8102643833" },
      { name: "SHIVANI KRI", phone: "7563912052" },
      { name: "SNEHA KUMARI", phone: "7295997451" },
      { name: "SUDHA KRI", phone: "9931051192" },
      { name: "SUMAN KUMARI", phone: "9560726946" },
      { name: "SUNITA KRI", phone: "8252764123" },
      { name: "VERSA KRI", phone: "7255032487" }
    ];

    // Calendar me default aaj ki date set karna
    function setDefaultDate() {
      const today = new Date();
      const yyyy = today.getFullYear();
      const mm = String(today.getMonth() + 1).padStart(2, '0');
      const dd = String(today.getDate()).padStart(2, '0');
      document.getElementById('billDate').value = `${yyyy}-${mm}-${dd}`;
    }

    // Date ko DD/MM/YYYY format me convert karna
    function getFormattedSelectedDate() {
      const val = document.getElementById('billDate').value;
      if (!val) return "";
      const p = val.split('-');
      return `${p[2]}/${p[1]}/${p[0]}`;
    }

    // Dropdown me bachho ka naam load karna
    function populateDropdown() {
      const select = document.getElementById('studentSelect');
      studentsData.forEach((st, idx) => {
        const opt = document.createElement('option');
        opt.value = idx;
        opt.textContent = `${st.name} (${st.phone || 'No Phone'})`;
        select.appendChild(opt);
      });
    }

    // Student select hone par fields auto-fill karna
    function onStudentSelectChange() {
      const select = document.getElementById('studentSelect');
      const val = select.value;
      if (val !== "") {
        const student = studentsData[val];
        document.getElementById('studentName').value = student.name;
        document.getElementById('parentPhone').value = student.phone || "";
        document.getElementById('prevDues').value = 0;
        document.getElementById('discountPaid').value = 0;
      }
      calculateBill();
    }

    // Realtime bill math calculation aur message preview generate karna
    function calculateBill() {
      const prev = parseFloat(document.getElementById('prevDues').value) || 0;
      const curr = parseFloat(document.getElementById('currDues').value) || 0;
      const minus = parseFloat(document.getElementById('discountPaid').value) || 0;

      let netPayable = (prev + curr) - minus;
      if (netPayable < 0) netPayable = 0;

      document.getElementById('mathBreakdown').innerText = 
        `विवरण: ₹${prev} (बकाया) + ₹${curr} (माह शुल्क) - ₹${minus} (छूट/अग्रिम)`;
      document.getElementById('totalPayableText').innerText = `₹ ${netPayable}`;

      const name = document.getElementById('studentName').value.trim() || "[विद्यार्थी का नाम]";
      const sClass = document.getElementById('studentClass').value.trim() || "12th";
      const month = document.getElementById('feeMonth').value;
      const bDate = getFormattedSelectedDate();

      let discountLine = "";
      if (minus > 0) {
        discountLine = `▫️ छूट / समायोजन: -₹${minus}\n`;
      }

      const message = 
`*मासिक शिक्षण शुल्क बिल (FEE BILL)* 📄
*संस्थान:* LUCENT COACHING CENTRE[span_21](start_span)[span_21](end_span)
*पता:* Near Mithila Eye Hospital, Musrigharari[span_22](start_span)[span_22](end_span)
*Helpline:* +91 8789524958[span_23](start_span)[span_23](end_span)
*Director:* Md Mahfooz Alam | *MD:* Md Nazir[span_24](start_span)[span_24](end_span)

सादर प्रणाम, आपके बच्चे का मासिक फीस बिल विवरण निम्नलिखित है:

▫️ विद्यार्थी का नाम: *${name}*
▫️ कक्षा (Class): *${sClass}*
▫️ बिल का महीना: *${month}*
▫️ बिल दिनांक: *${bDate}*
--------------------------------
▫️ पिछला बकाया शुल्क: ₹${prev}
▫️ चालू माह शुल्क: ₹${curr}
${discountLine}--------------------------------
*कुल देय बिल राशि: ₹${netPayable}*
--------------------------------

💳 *ऑनलाइन भुगतान (PhonePe / UPI):*
• नाम: *Md Mahfooz*[span_25](start_span)[span_25](end_span)
• PhonePe नंबर: *8789524958*[span_26](start_span)[span_26](end_span)[span_27](start_span)[span_27](end_span)
• UPI ID: *8789524958-2@ibl*[span_28](start_span)[span_28](end_span)
*(ऑनलाइन भुगतान के बाद कृपया स्क्रीनशॉट इसी नंबर पर भेजें)*

धन्यवाद,
*LUCENT COACHING CENTRE MUSRIGHARARI*[span_29](start_span)[span_29](end_span)`;

      document.getElementById('messagePreview').innerText = message;
      return { message, netPayable, prev, curr, minus, name, sClass, month, bDate };
    }

    // Print ya PDF save trigger function[span_30](start_span)[span_30](end_span)
    function printBillPDF() {
      const data = calculateBill();
      if (!document.getElementById('studentName').value.trim()) {
        alert("कृपया पहले छात्र का नाम चुनें!");
        return;
      }

      document.getElementById('billNo').innerText = 'LCC-BILL-' + Math.floor(100 + Math.random() * 900);
      document.getElementById('billDateDisplay').innerText = data.bDate;
      document.getElementById('bStudentName').innerText = data.name;
      document.getElementById('bClass').innerText = data.sClass;
      document.getElementById('bPhone').innerText = document.getElementById('parentPhone').value.trim() || 'N/A';
      document.getElementById('bMonth').innerText = data.month;
      document.getElementById('bPrevDue').innerText = `₹${data.prev}`;
      document.getElementById('bCurrFee').innerText = `₹${data.curr}`;
      document.getElementById('bDiscount').innerText = `₹${data.minus}`;
      document.getElementById('bTotalPayable').innerText = `₹${data.netPayable}`;

      window.print();
    }

    // WhatsApp ya SMS dispatch function[span_31](start_span)[span_31](end_span)
    function sendBillMessage(type) {
      const data = calculateBill();
      let phone = document.getElementById('parentPhone').value.trim();

      if (!document.getElementById('studentName').value.trim()) {
        alert("कृपया पहले छात्र का नाम चुनें!");
        return;
      }
      if (!phone) {
        alert("कृपया अभिभावक का मोबाइल नंबर दर्ज करें!");
        return;
      }

      let cleanPhone = phone.replace(/[^0-9]/g, '');

      if (type === 'whatsapp') {
        let waNumber = cleanPhone;
        if (waNumber.length === 10) {
          waNumber = '91' + waNumber;
        }
        const waURL = `https://wa.me/${waNumber}?text=${encodeURIComponent(data.message)}`;
        window.open(waURL, '_blank');[span_32](start_span)[span_32](end_span)
      } else if (type === 'sms') {
        const plainMsg = 
`फीस बिल (LUCENT COACHING CENTRE):
छात्र: ${data.name} (${data.sClass})
माह: ${data.month}
दिनांक: ${data.bDate}
कुल देय बिल: Rs.${data.netPayable}
PhonePe: 8789524958 (Md Mahfooz)
हेल्पलाइन: 8789524958[span_33](start_span)[span_33](end_span)[span_34](start_span)[span_34](end_span)[span_35](start_span)[span_35](end_span)`;

        const smsURL = `sms:${cleanPhone}?body=${encodeURIComponent(plainMsg)}`;
        window.location.href = smsURL;[span_36](start_span)[span_36](end_span)
      }
    }

    // Window load par execution trigger
    window.onload = function() {
      setDefaultDate();
      populateDropdown();
      calculateBill();
    };
  </script>
</body>
</html>
