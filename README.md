# don-saab-ki-repo
my herupa waalo ne kaha tha.
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>APK Generator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }
    .container {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      text-align: center;
    }
    input[type="file"] {
      margin: 15px 0;
    }
    button {
      padding: 10px 20px;
      border: none;
      background: #4CAF50;
      color: white;
      border-radius: 5px;
      cursor: pointer;
    }
    .apk-link {
      margin-top: 20px;
      display: none;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>APK Generator</h2>
    <p>ZIP Project Upload करो और APK पाओ</p>
    <input type="file" id="zipFile" accept=".zip" />
    <br />
    <button onclick="generateAPK()">Generate APK</button>
    <div class="apk-link" id="apkLink">
      <p>APK तैयार है:</p>
      <a id="downloadLink" href="#" download>Download APK</a>
    </div>
  </div>  <script>
    function generateAPK() {
      const fileInput = document.getElementById("zipFile");
      const apkLink = document.getElementById("apkLink");
      const downloadLink = document.getElementById("downloadLink");
      if (!fileInput.files.length) {
        alert("कृपया ZIP फाइल अपलोड करें");
        return;
      }
      // Dummy APK generation simulation
      setTimeout(() => {
        apkLink.style.display = "block";
        downloadLink.href = "game.apk";
        downloadLink.textContent = "Download game.apk";
      }, 2000);
    }
  </script></body>
</html>
