<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hộp quà Mỹ Kỳ</title>
  <style>
    body {
      margin: 0;
      background-color: #f8f8f8;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial, sans-serif;
    }
    .gift-box {
      position: relative;
      width: 200px;
      height: 200px;
      background: #ff3366;
      border-radius: 10px;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
      cursor: pointer;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      transition: 0.5s ease-in-out;
    }
    .gift-box::before {
      content: "";
      position: absolute;
      width: 40px;
      height: 200%;
      background: gold;
      transform: rotate(45deg);
      left: 50%;
      top: 0;
      transition: 0.5s;
    }
    .gift-box.open::before {
      transform: rotate(90deg);
      top: -50%;
    }
    .lid {
      position: absolute;
      top: -40px;
      width: 100%;
      height: 50px;
      background: #ff6699;
      border-radius: 10px 10px 0 0;
      transition: 0.5s ease-in-out;
    }
    .gift-box.open .lid {
      top: -120px;
    }
    .cake {
      position: absolute;
      bottom: -100px;
      width: 100px;
      height: 100px;
      background: #fff;
      border-radius: 50%;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 14px;
      color: #ff3366;
      font-weight: bold;
      transition: 0.5s ease-in-out;
    }
    .gift-box.open .cake {
      bottom: 20px;
    }
  </style>
</head>
<body>
  <div class="gift-box" onclick="openBox()">
    <div class="lid"></div>
    <div class="cake">Mỹ Kỳ</div>
  </div>

  <script>
    function openBox() {
      const box = document.querySelector('.gift-box');
      box.classList.toggle('open');
    }
  </script>
</body>
</htm
