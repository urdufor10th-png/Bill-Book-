# Bill-Book-
Biling Related Register 
<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>फीस रिमाइंडर व ऑटो-बिलिंग पोर्टल - LUCENT COACHING CENTRE</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700;900&display=swap" rel="stylesheet">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Roboto', sans-serif; }
    body { background-color: #cbd5e1; color: #0f172a; padding: 20px 10px; }

    /* RECTANGULAR SHARP DESIGN */
    .portal-card {
      max-width: 680px;
      margin: 0 auto;
      background: #ffffff;
      border: 3px solid #002244;
      border-radius: 0px;
      box-shadow: 7px 7px 0px rgba(0, 34, 68, 0.9);
    }

    .portal-header {
      background: #002b49;
      color: #ffffff;
      padding: 16px 20px;
      text-align: center;
      border-bottom: 3px solid #002244;
    }
    .portal-header h1 {
      font-size: 18px;
      font-weight: 900;
      letter-spacing: 0.5px;
      text-transform: uppercase;
    }
    .portal-header p {
      font-size: 12.5px;
      color: #38bdf8;
      margin-top: 4px;
      font-weight: 600;
    }

    .portal-body { padding: 20px; }

    .grid-2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin-bottom: 12px;
    }
    .grid-3 {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 10px;
      margin-bottom: 14px;
    }

    .form-cell { display: flex; flex-direction: column; }
    .form-cell label {
      font-size: 12px;
      font-weight: 800;
      color: #1e293b;
      margin-bottom: 5px;
      text-transform: uppercase;
    }
    .form-cell input, .form-cell select {
      width: 100%;
      padding: 10px 12px;
      font-size: 13.5px;
      border: 2px solid #334155;
      border-radius: 0px;
      background: #ffffff;
      color: #0f172a;
      outline: none;
      font-weight: 600;
    }
    .form-cell input:focus, .form-cell select:focus {
      border-color: #0284c7;
      background: #f0f9ff;
    }

    /* BADA DROP-DOWN FOR MONTH */
    .month-select-large {
      padding: 12px 14px !important;
      font-size: 16px !important;
      font-weight: 800 !important;
      color: #003366 !important;
      cursor: pointer;
      border: 2.5px solid #003366 !important;
      background: #f8fafc !important;
    }

    /* CALCULATION BAR */
    .calc-bar {
      background: #f8fafc;
      border: 2px solid #0284c7;
      border-radius: 0px;
      padding: 12px 14px;
      margin: 15px 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 10px;
    }
    .calc-details {
      font-size: 12px;
      color: #475569;
      font-weight: 700;
    }
    .calc-total {
      text-align: right;
    }
    .calc-total span {
      font-size: 11px;
      font-weight: 800;
      color: #003366;
      display: block;
      text-transform: uppercase;
    }
    .calc-total strong {
      font-size: 24px;
      color: #dc2626;
      font-weight: 900;
    }

    /* PHONEPE DETAILS BOX */
    .payment-box {
      background: #faf5ff;
      border: 2px dashed #9333ea;
      border-radius: 0px;
      padding: 10px 12px;
      margin-bottom: 15px;
      font-size: 12.5px;
    }
    .payment-box strong { color: #581c87; }

    /* PREVIEW */
    .preview-box {
      background: #f8fafc;
      border: 2px solid #94a3b8;
      border-radius: 0px;
      padding: 12px;
      font-size: 12.5px;
      line-height: 1.6;
      color: #1e293b;
      white-space: pre-wrap;
      margin-bottom: 16px;
      max-height: 200px;
      overflow-y: auto;
    }

    /* DUAL ACTION BUTTONS */
    .button-group-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
    }

    .btn-action {
      width: 100%;
      border-radius: 0px;
      padding: 14px;
      font-size: 15px;
      font-weight: 900;
      cursor: pointer;
      text-transform: uppercase;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      transition: all 0.1s ease;
    }

    .btn-whatsapp {
      background: #16a34a;
      color: #ffffff;
      border: 2px solid #14532d;
      box-shadow: 4px 4px 0px #14532d;
    }
    .btn-whatsapp:hover {
      background: #15803d;
      transform: translate(1px, 1px);
      box-shadow: 3px 3px 0px #14532d;
    }

    .btn-sms {
      background: #0284c7;
      color: #ffffff;
      border: 2px solid #0369a1;
      box-shadow: 4px 4px 0px #0369a1;
    }
    .btn-sms:hover {
      background: #0369a1;
      transform: translate(1px, 1px);
      box-shadow: 3px 3px 0px #0369a1;
    }

    .btn-action:active {
      transform: translate(4px, 4px);
      box-shadow: none;
    }

    @media (max-width: 600px) {
      .grid-2, .grid-3, .button-group-row { grid-template-columns: 1fr; }
      .calc-bar { flex-direction: column; align-items: flex-start; }
      .calc-total { text-align: left; }
    }
  </style>
</head>
<body>

  <div class="portal-card">
    <div class="portal-header">
      <h1>LUCENT COACHING CENTRE MUSRIGHARARI</h1>
      <p>छात्र फीस प्रबंधन एवं बिलिंग सिस्टम</p>
    </div>

    <div class="portal-body">
      <!-- 1. Student Selection -->
      <div class="grid-2">
        <div class="form-cell">
          <label>छात्र चुनें (OkCredit लिस्ट से):</label>
          <select id="studentSelect" onchange="onStudentSelectChange()">
            <option value="">-- छात्र का नाम चुनें --</option>
          </select>
        </div>
        <div class="form-cell">
          <label>छात्र का नाम (एडिट योग्य):</label>
          <input type="text" id="studentName" placeholder="छात्र का नाम" oninput="calculateTotal()">
        </div>
      </div>

      <!-- 2. Phone & Class -->
      <div class="grid-2">
        <div class="form-cell">
          <label>अभिभावक का मोबाइल नंबर:</label>
          <input type="tel" id="parentPhone" placeholder="10 अंकों का मोबाइल नंबर">
        </div>
        <div class="form-cell">
          <label>कक्षा / सेक्शन (Class):</label>
          <input type="text" id="studentClass" value="12th" oninput="calculateTotal()">
        </div>
      </div>

      <!-- 3. Month Dropdown (English & Large) -->
      <div class="form-cell" style="margin-bottom: 14px;">
        <label>SELECT FEE MONTH (महीना चुनें):</label>
        <select id="feeMonth" class="month-select-large" onchange="calculateTotal()">
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

      <!-- 4. Dynamic Math Row: Prev + Curr - Minus -->
      <div class="grid-3">
        <div class="form-cell">
          <label>पिछला बकाया (+ ₹):</label>
          <input type="number" id="prevDues" value="0" min="0" oninput="calculateTotal()">
        </div>
        <div class="form-cell">
          <label>चालू माह शुल्क (+ ₹):</label>
          <input type="number" id="currDues" value="450" min="0" oninput="calculateTotal()">
        </div>
        <div class="form-cell">
          <label>छूट / अग्रिम (- ₹):</label>
          <input type="number" id="discountPaid" value="0" min="0" oninput="calculateTotal()">
        </div>
      </div>

      <!-- Math Summary Box -->
      <div class="calc-bar">
        <div class="calc-details" id="mathBreakdown">
          गणना: ₹0 (बकाया) + ₹450 (माह शुल्क) - ₹0 (छूट)
        </div>
        <div class="calc-total">
          <span>कुल देय राशि (Total Payable)</span>
          <strong id="totalPayableText">₹ 450</strong>
        </div>
      </div>

      <!-- PhonePe Payment Info -->
      <div class="payment-box">
        <strong>🟣 PhonePe / UPI भुगतान विवरण:</strong><br>
        नाम: <b>Md Mahfooz</b> | PhonePe: <b>8789524958</b> | UPI: <b>8789524958-2@ibl</b>
      </div>

      <!-- Preview Box -->
      <label style="font-size: 11px; font-weight: 800; color: #475569; text-transform: uppercase; margin-bottom: 4px; display: block;">
        लाइव मेसेज प्रीव्यू (यही मेसेज भेजा जाएगा):
      </label>
      <div class="preview-box" id="messagePreview"></div>

      <!-- Action Buttons: WhatsApp & Normal Message -->
      <div class="button-group-row">
        <button type="button" class="btn-action btn-whatsapp" onclick="sendMessage('whatsapp')">
          <span>💬</span> WhatsApp पर भेजें
        </button>
        <button type="button" class="btn-action btn-sms" onclick="sendMessage('sms')">
          <span>✉️</span> SMS (संदेश) भेजें
        </button>
      </div>
    </div>
  </div>

  <script>
    // Sirf Naam aur Mobile Number (Bakaya hata diya gaya hai)
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

    function populateDropdown() {
      const select = document.getElementById('studentSelect');
      studentsData.forEach((st, idx) => {
        const opt = document.createElement('option');
        opt.value = idx;
        opt.textContent = `${st.name} (${st.phone || 'No Number'})`;
        select.appendChild(opt);
      });
    }

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
      calculateTotal();
    }

    function getDueDate10DaysLater() {
      const date = new Date();
      date.setDate(date.getDate() + 10);
      const day = String(date.getDate()).padStart(2, '0');
      const month = String(date.getMonth() + 1).padStart(2, '0');
      const year = date.getFullYear();
      return `${day}/${month}/${year}`;
    }

    function calculateTotal() {
      const prev = parseFloat(document.getElementById('prevDues').value) || 0;
      const curr = parseFloat(document.getElementById('currDues').value) || 0;
      const minus = parseFloat(document.getElementById('discountPaid').value) || 0;

      let netPayable = (prev + curr) - minus;
      if (netPayable < 0) netPayable = 0;

      document.getElementById('mathBreakdown').innerText = 
        `गणना: ₹${prev} (बकाया) + ₹${curr} (माह शुल्क) - ₹${minus} (छूट/अग्रिम)`;
      document.getElementById('totalPayableText').innerText = `₹ ${netPayable}`;

      const name = document.getElementById('studentName').value.trim() || "[विद्यार्थी का नाम]";
      const sClass = document.getElementById('studentClass').value.trim() || "12th";
      const month = document.getElementById('feeMonth').value;
      const dueDate = getDueDate10DaysLater();

      let discountLine = "";
      if (minus > 0) {
        discountLine = `▫️ दी गई छूट / प्राप्त राशि: -₹${minus}\n`;
      }

      const message = 
`*सादर प्रणाम (मासिक फीस सूचना)* 🙏
*संस्थान:* LUCENT COACHING CENTRE MUSRIGHARARI

माननीय अभिभावक, आपके बच्चे *${name}* (कक्षा: *${sClass}*) का मासिक शिक्षण शुल्क विवरण निम्नलिखित है:

▫️ पिछला बकाया शुल्क: ₹${prev}
▫️ चालू माह शुल्क (${month}): ₹${curr}
${discountLine}--------------------------------
*कुल देय राशि: ₹${netPayable}*
--------------------------------

💳 *ऑनलाइन भुगतान (PhonePe / UPI):*
• नाम: *Md Mahfooz*
• PhonePe नंबर: *8789524958*
• UPI ID: *8789524958-2@ibl*
*(ऑनलाइन भुगतान के बाद कृपया स्क्रीनशॉट इसी नंबर पर भेजें)*

⚠️ *अनुरोध:* आपसे सविनय निवेदन है कि संस्थान के पठन-पाठन कार्य को सुचारू रूप से चलाने हेतु आगामी *10 दिनों के अंदर (दिनांक: ${dueDate} तक)* इस बकाया शुल्क को जमा कराने की कृपा करें।

यदि आपने यह शुल्क पहले ही जमा कर दिया है, तो कृपया इस संदेश को अनदेखा करें।

धन्यवाद,
*LUCENT COACHING CENTRE MUSRIGHARARI*`;

      document.getElementById('messagePreview').innerText = message;
      return { message, netPayable };
    }

    function sendMessage(type) {
      let rawPhone = document.getElementById('parentPhone').value.trim();
      const name = document.getElementById('studentName').value.trim();

      if (!name) {
        alert("कृपया छात्र का नाम चुनें या दर्ज करें!");
        return;
      }
      if (!rawPhone) {
        alert("कृपया अभिभावक का मोबाइल नंबर दर्ज करें!");
        return;
      }

      let cleanPhone = rawPhone.replace(/[^0-9]/g, '');
      const { message } = calculateTotal();

      if (type === 'whatsapp') {
        let waNumber = cleanPhone;
        if (waNumber.length === 10) {
          waNumber = '91' + waNumber;
        }
        const whatsappURL = `https://wa.me/${waNumber}?text=${encodeURIComponent(message)}`;
        window.open(whatsappURL, '_blank');
      } else if (type === 'sms') {
        const plainMsg = message.replace(/\*/g, '');
        const smsURL = `sms:${cleanPhone}?body=${encodeURIComponent(plainMsg)}`;
        window.location.href = smsURL;
      }
    }

    window.onload = function() {
      populateDropdown();
      calculateTotal();
    };
  </script>
</body>
</html>
