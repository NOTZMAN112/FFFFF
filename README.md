        <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Contact Info - Zack</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f8fb;
      color: #333;
      padding: 40px;
      text-align: center;
    }
    h1 {
      color: #2b78e4;
    }
    .contact-card {
      background-color: #fff;
      border-radius: 10px;
      padding: 30px;
      max-width: 400px;
      margin: 0 auto;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    .contact-row {
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 15px 0;
      font-size: 16px;
    }
    .contact-label {
      font-weight: bold;
      margin-right: 10px;
    }
    .contact-text {
      margin-right: 10px;
    }
    .copy-text {
      color: #2b78e4;
      cursor: pointer;
      font-weight: 600;
      user-select: none;
      transition: color 0.3s;
    }
    .copy-text:hover {
      color: #1a5fc0;
      text-decoration: underline;
    }
    .copied-msg {
      font-size: 12px;
      color: green;
      margin-left: 10px;
      display: none;
      user-select: none;
    }
    a {
      color: #2b78e4;
      text-decoration: none;
      font-weight: bold;
    }
    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <div class="contact-card">
    <h1>Contact Info</h1>

    <div class="contact-row">
      <span class="contact-label">📞 Phone:</span>
      <span class="contact-text" id="phone">1 (567) 438-3989</span>
      <span class="copy-text" onclick="copyToClipboard('phone', this)">Copy</span>
      <span class="copied-msg">Copied!</span>
    </div>

    <div class="contact-row">
      <span class="contact-label">📧 Email:</span>
      <span class="contact-text" id="email">chaffinzack6@gmail.com</span>
      <span class="copy-text" onclick="copyToClipboard('email', this)">Copy</span>
      <span class="copied-msg">Copied!</span>
    </div>

    <p><strong>🎮 Roblox:</strong> <a href="https://www.roblox.com/users/8821344205/profile" target="_blank" rel="noopener noreferrer">JANDLE_RBLX</a></p>
  </div>

  <script>
    function copyToClipboard(id, element) {
      const text = document.getElementById(id).innerText;
      navigator.clipboard.writeText(text).then(() => {
        const msg = element.nextElementSibling;
        msg.style.display = 'inline';
        setTimeout(() => {
          msg.style.display = 'none';
        }, 1500);
      });
    }
  </script>
</body>
</html>
