<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Yêu anhhhh khônggg?</title>
  <style>
    body {
      text-align: center;
      font-family: 'Arial', sans-serif;
      background-color: #ffeef0;
      margin-top: 100px;
    }
    h1 {
      font-size: 28px;
      color: #333;
    }
    .cute-img {
      width: 120px;
      margin-bottom: 20px;
    }
    #yesBtn, #noBtn {
      font-size: 20px;
      padding: 15px 30px;
      margin: 20px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
    }
    #yesBtn {
      background-color: #ff6b81;
      color: white;
      z-index: 1;
      position: relative;
    }
    #noBtn {
      background-color: #7f8fa6;
      color: white;
    }
  </style>
</head>
<body>

  <img src="https://i.imgur.com/dJbT56j.png" alt="cute" class="cute-img">
  <h1>Em có yêu anhhhh khônggg 🥺</h1>
  <button id="yesBtn">Có</button>
  <button id="noBtn">Không</button>

  <script>
    const yesBtn = document.getElementById('yesBtn');
    const noBtn = document.getElementById('noBtn');

    noBtn.addEventListener('click', () => {
      noBtn.disabled = true;
      noBtn.innerText = 'Không được chọn cái này!';
      
      // Phóng to nút "Có" dần dần
      let scale = 1;
      const grow = setInterval(() => {
        scale += 0.1;
        yesBtn.style.transform = scale(${scale});
        if (scale >= 20) {
          clearInterval(grow);
          document.body.innerHTML = "<h1 style='color:white;background:#ff6b81;padding:50px'>Anh biết mà 🥰 Cảm ơn vợ đã yêu anh! 💖</h1>";
        }
      }, 100);
    });

    yesBtn.addEventListener('click', () => {
      alert("Anh biết mà 🥰 Yêu vợ nhiều lắm ♥");
    });
  </script>

</body>
</html>
