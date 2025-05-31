<!DOCTYPE html>
<html lang="vi">
<head>
  <link rel="icon" href="/logo.png" />

  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Đếm ngược đến Tết</title>
  <link href="https://fonts.googleapis.com/css2?family=Baloo+2&display=swap" rel="stylesheet" />
  <style>
    body {
      margin: 0;
      font-family: 'Baloo 2', cursive;
      background: radial-gradient(circle at top, #fff3e0, #ffe0b2);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      padding: 20px;
      color: #4e342e;
      transition: background-color 0.5s, color 0.5s;
    }
    body.dark {
      background: radial-gradient(circle at top, #1a1a1a, #333);
      color: #ddd;
    }
    h1 {
      font-size: 2.5rem;
      color: #d84315;
      margin-bottom: 10px;
    }
    body.dark h1 {
      color: #ff7043;
    }
    select {
      padding: 10px 15px;
      font-size: 1.1rem;
      border-radius: 8px;
      background-color: #fff8e1;
      border: none;
      margin-bottom: 20px;
      cursor: pointer;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      transition: background-color 0.5s, color 0.5s;
    }
    body.dark select {
      background-color: #444;
      color: #ddd;
    }
    .countdown {
      background: #ffffffdd;
      padding: 25px 35px;
      border-radius: 16px;
      font-size: 1.8rem;
      text-align: center;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      max-width: 500px;
      transition: background-color 0.5s, color 0.5s;
    }
    body.dark .countdown {
      background: #222222dd;
      color: #eee;
      box-shadow: 0 4px 12px rgba(255, 255, 255, 0.2);
    }
    .animal {
      font-size: 1.2rem;
      color: #6d4c41;
      margin-top: 10px;
      transition: color 0.5s;
    }
    body.dark .animal {
      color: #bbb;
    }
    canvas {
      position: fixed;
      top: 0;
      left: 0;
      z-index: 999;
      pointer-events: none;
    }
  </style>
</head>
<body>
  <h1>🎉 Đếm ngược đến Tết Nguyên Đán 🎉</h1>

  <label for="year">Chọn năm:</label>
  <select id="year"></select>

  <div class="countdown" id="countdown">Đang tải...</div>
  <div class="animal" id="animal"></div>

  <canvas id="fireworksCanvas"></canvas>

  <script>
    // Dữ liệu ngày Tết các năm
    const tetDates = {
      2026: '2026-02-17T00:00:00',
      2027: '2027-02-06T00:00:00',
      2028: '2028-01-26T00:00:00',
      2029: '2029-02-13T00:00:00',
      2030: '2030-02-03T00:00:00',
      2031: '2031-01-23T00:00:00',
      2032: '2032-02-11T00:00:00',
      2033: '2033-01-31T00:00:00',
      2034: '2034-01-20T00:00:00',
      2035: '2035-02-08T00:00:00',
      2036: '2036-01-28T00:00:00',
      2037: '2037-02-15T00:00:00',
      2038: '2038-02-04T00:00:00',
      2039: '2039-01-24T00:00:00',
      2040: '2040-02-12T00:00:00',
      2041: '2041-02-01T00:00:00',
      2042: '2042-01-22T00:00:00',
      2043: '2043-02-10T00:00:00',
      2044: '2044-01-30T00:00:00',
      2045: '2045-02-17T00:00:00',
      2046: '2046-02-06T00:00:00',
      2047: '2047-01-26T00:00:00',
      2048: '2048-02-14T00:00:00',
      2049: '2049-02-03T00:00:00',
      2050: '2050-01-23T00:00:00',
    };

    // 12 con giáp
    const zodiac = ['Tý 🐭', 'Sửu 🐮', 'Dần 🐯', 'Mão 🐰', 'Thìn 🐲', 'Tỵ 🐍', 'Ngọ 🐴', 'Mùi 🐐', 'Thân 🐵', 'Dậu 🐔', 'Tuất 🐶', 'Hợi 🐷'];

    // 10 Can, 12 Chi để tạo Can Chi
    const can = ['Giáp', 'Ất', 'Bính', 'Đinh', 'Mậu', 'Kỷ', 'Canh', 'Tân', 'Nhâm', 'Quý'];
    const chi = ['Tý', 'Sửu', 'Dần', 'Mão', 'Thìn', 'Tỵ', 'Ngọ', 'Mùi', 'Thân', 'Dậu', 'Tuất', 'Hợi'];

    const baseYear = 1984; // Năm Giáp Tý

    const yearSelect = document.getElementById('year');
    const countdownEl = document.getElementById('countdown');
    const animalEl = document.getElementById('animal');
    const canvas = document.getElementById('fireworksCanvas');
    const ctx = canvas.getContext('2d');

    // Chế độ tối/ngày theo giờ
    function updateTheme() {
      const hour = new Date().getHours();
      if (hour >= 19 || hour < 6) {
        document.body.classList.add('dark');
      } else {
        document.body.classList.remove('dark');
      }
    }
    updateTheme();
    setInterval(updateTheme, 60000);

    function updateCanvasSize() {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    }
    window.addEventListener('resize', updateCanvasSize);
    updateCanvasSize();

    // Tính Can Chi của năm
    function getCanChi(year) {
      const canIndex = (year - baseYear) % 10;
      const chiIndex = (year - baseYear) % 12;
      return can[canIndex < 0 ? canIndex + 10 : canIndex] + ' ' + chi[chiIndex < 0 ? chiIndex + 12 : chiIndex];
    }

    // Lấy con giáp của năm
    function getZodiac(year) {
      const index = (year - 2020) % 12;
      return zodiac[(index + 12) % 12];
    }

    function populateYears() {
      const now = new Date();
      yearSelect.innerHTML = '';
      for (let y = 2026; y <= 2050; y++) {
        if (tetDates[y]) {
          const tetDate = new Date(tetDates[y]);
          if (tetDate > now) {
            const option = document.createElement('option');
            option.value = y;
            option.textContent = `${y} - ${getCanChi(y)} (${getZodiac(y)})`;
            yearSelect.appendChild(option);
          }
        }
      }
      if (yearSelect.options.length > 0) {
        yearSelect.value = yearSelect.options[0].value;
      }
    }

    let timer;

    function updateCountdown() {
      const selectedYear = parseInt(yearSelect.value);
      const tetDate = new Date(tetDates[selectedYear]);
      const now = new Date();

      if (!tetDate) {
        countdownEl.textContent = 'Không có dữ liệu ngày Tết cho năm này.';
        animalEl.textContent = '';
        return;
      }

      const diff = tetDate - now;
      if (diff <= 0) {
        countdownEl.textContent = `🎉 Đã đến Tết năm ${selectedYear}! Chúc mừng năm mới ${getCanChi(selectedYear)} ${getZodiac(selectedYear)}! 🎉`;
        animalEl.textContent = '';
        startFireworks();
        clearInterval(timer);
        return;
      }

      const days = Math.floor(diff / (1000 * 60 * 60 * 24));
      const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const minutes = Math.floor((diff / (1000 * 60)) % 60);
      const seconds = Math.floor((diff / 1000) % 60);

      countdownEl.textContent = `Còn ${days} ngày ${hours} giờ ${minutes} phút ${seconds} giây đến Tết ${selectedYear}`;
      animalEl.textContent = `Năm ${selectedYear} là năm con: ${getZodiac(selectedYear)}`;
    }

    yearSelect.addEventListener('change', () => {
      clearInterval(timer);
      stopFireworks();
      updateCountdown();
      timer = setInterval(updateCountdown, 1000);
    });

    // ==== FIREWORKS EFFECT ==== //
    const fireworks = [];
    const particles = [];

    class Firework {
      constructor(sx, sy, tx, ty) {
        this.x = sx;
        this.y = sy;
        this.sx = sx;
        this.sy = sy;
        this.tx = tx;
        this.ty = ty;
        this.distanceToTarget = this.calcDistance(sx, sy, tx, ty);
        this.distanceTraveled = 0;
        this.coordinates = [];
        this.coordinateCount = 3;
        while(this.coordinateCount--) {
          this.coordinates.push([this.x, this.y]);
        }
        this.angle = Math.atan2(ty - sy, tx - sx);
        this.speed = 3 + Math.random() * 3;
        this.acceleration = 1.05;
        this.brightness = Math.random() * 50 + 50;
        this.targetRadius = 1;
      }
      update(index) {
        this.coordinates.pop();
        this.coordinates.unshift([this.x, this.y]);
        if(this.targetRadius < 8) {
          this.targetRadius += 0.3;
        } else {
          this.targetRadius = 1;
        }
        this.speed *= this.acceleration;
        let vx = Math.cos(this.angle) * this.speed;
        let vy = Math.sin(this.angle) * this.speed;
        this.distanceTraveled = this.calcDistance(this.sx, this.sy, this.x + vx, this.y + vy);
        if(this.distanceTraveled >= this.distanceToTarget) {
          createParticles(this.tx, this.ty);
          fireworks.splice(index, 1);
        } else {
          this.x += vx;
          this.y += vy;
        }
      }
      draw() {
        ctx.beginPath();
        ctx.moveTo(this.coordinates[this.coordinates.length - 1][0], this.coordinates[this.coordinates.length - 1][1]);
        ctx.lineTo(this.x, this.y);
        ctx.strokeStyle = `hsl(${Math.random() * 360}, 100%, ${this.brightness}%)`;
        ctx.stroke();

        ctx.beginPath();
        ctx.arc(this.tx, this.ty, this.targetRadius, 0, Math.PI * 2);
        ctx.stroke();
      }
      calcDistance(aX, aY, bX, bY) {
        let x = bX - aX;
        let y = bY - aY;
        return Math.sqrt(x * x + y * y);
      }
    }

    class Particle {
      constructor(x, y) {
        this.x = x;
        this.y = y;
        this.coordinates = [];
        this.coordinateCount = 5;
        while(this.coordinateCount--) {
          this.coordinates.push([this.x, this.y]);
        }
        this.angle = Math.random() * Math.PI * 2;
        this.speed = Math.random() * 5 + 1;
        this.friction = 0.95;
        this.gravity = 0.7;
        this.hue = Math.floor(Math.random() * 360);
        this.brightness = Math.random() * 50 + 50;
        this.alpha = 1;
        this.decay = Math.random() * 0.015 + 0.015;
      }
      update(index) {
        this.coordinates.pop();
        this.coordinates.unshift([this.x, this.y]);
        this.speed *= this.friction;
        this.x += Math.cos(this.angle) * this.speed;
        this.y += Math.sin(this.angle) * this.speed + this.gravity;
        this.alpha -= this.decay;
        if(this.alpha <= 0) {
          particles.splice(index, 1);
        }
      }
      draw() {
        ctx.beginPath();
        ctx.moveTo(this.coordinates[this.coordinates.length - 1][0], this.coordinates[this.coordinates.length - 1][1]);
        ctx.lineTo(this.x, this.y);
        ctx.strokeStyle = `hsla(${this.hue}, 100%, ${this.brightness}%, ${this.alpha})`;
        ctx.stroke();
      }
    }

    function createParticles(x, y) {
      let particleCount = 30;
      while(particleCount--) {
        particles.push(new Particle(x, y));
      }
    }

    let animationId;
    let fireworksInterval;

    function loop() {
      ctx.globalCompositeOperation = 'destination-out';
      ctx.fillStyle = 'rgba(0, 0, 0, 0.3)';
      ctx.fillRect(0, 0, canvas.width, canvas.height);
      ctx.globalCompositeOperation = 'lighter';

      let i = fireworks.length;
      while(i--) {
        fireworks[i].draw();
        fireworks[i].update(i);
      }

      let j = particles.length;
      while(j--) {
        particles[j].draw();
        particles[j].update(j);
      }

      animationId = requestAnimationFrame(loop);
    }

    function startFireworks() {
      if (fireworksInterval) return;
      fireworksInterval = setInterval(() => {
        let sx = Math.random() * canvas.width;
        let sy = canvas.height;
        let tx = Math.random() * canvas.width;
        let ty = Math.random() * canvas.height / 2;
        fireworks.push(new Firework(sx, sy, tx, ty));
      }, 400);
      loop();
    }

    function stopFireworks() {
      clearInterval(fireworksInterval);
      fireworksInterval = null;
      fireworks.length = 0;
      particles.length = 0;
      cancelAnimationFrame(animationId);
      ctx.clearRect(0, 0, canvas.width, canvas.height);
    }

    // Khởi tạo năm và countdown
    populateYears();
    updateCountdown();
    timer = setInterval(updateCountdown, 1000);
  </script>
</body>
</html>
