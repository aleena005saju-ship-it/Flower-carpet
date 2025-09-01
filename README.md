<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Pookalam with CSS</title>
  <style>
    body {
      background: #fdf6e3;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .pookalam {
      position: relative;
      width: 400px;
      height: 400px;
    }

    .circle {
      position: absolute;
      border-radius: 50%;
      border: 5px solid transparent;
    }

    .layer1 {
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, #ff00ff, #ffccff);
      z-index: 1;
    }

    .layer2 {
      width: 300px;
      height: 300px;
      background: radial-gradient(circle, #ffcc00, #fff176);
      top: 50px;
      left: 50px;
      z-index: 2;
    }

    .layer3 {
      width: 200px;
      height: 200px;
      background: radial-gradient(circle, #ff5722, #ffccbc);
      top: 100px;
      left: 100px;
      z-index: 3;
    }

    .layer4 {
      width: 100px;
      height: 100px;
      background: radial-gradient(circle, #4caf50, #a5d6a7);
      top: 150px;
      left: 150px;
      z-index: 4;
    }

    /* Flower petals around the center */
    .petal {
      position: absolute;
      width: 60px;
      height: 100px;
      background: radial-gradient(ellipse at center, #e91e63 0%, #f8bbd0 100%);
      border-radius: 50% 50% 50% 50%;
      transform-origin: bottom center;
      top: 50%;
      left: 50%;
      margin-top: -100px;
      margin-left: -30px;
      z-index: 0;
    }

    /* Generate multiple petals rotated */
    .petal:nth-child(5) { transform: rotate(0deg) translateY(-130px); }
    .petal:nth-child(6) { transform: rotate(45deg) translateY(-130px); }
    .petal:nth-child(7) { transform: rotate(90deg) translateY(-130px); }
    .petal:nth-child(8) { transform: rotate(135deg) translateY(-130px); }
    .petal:nth-child(9) { transform: rotate(180deg) translateY(-130px); }
    .petal:nth-child(10) { transform: rotate(225deg) translateY(-130px); }
    .petal:nth-child(11) { transform: rotate(270deg) translateY(-130px); }
    .petal:nth-child(12) { transform: rotate(315deg) translateY(-130px); }
  </style>
</head>
<body>

<div class="pookalam">
  <!-- Concentric circles -->
  <div class="circle layer1"></div>
  <div class="circle layer2"></div>
  <div class="circle layer3"></div>
  <div class="circle layer4"></div>

  <!-- Petals around -->
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
  <div class="petal"></div>
</div>

</body>
</html>
