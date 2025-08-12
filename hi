<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Flowers for You</title>

<!-- Import romantic font from Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">

<style>
  body {
    margin: 0;
    background: #fff0f6;
    overflow: hidden;
    font-family: 'Great Vibes', cursive; /* romantic font */
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: #d81e5b; /* bright pink text */
    user-select: none;
  }
  h1 {
    font-size: 3rem; /* bigger for elegance */
    margin-bottom: 2rem;
    text-align: center;
    font-weight: normal;
  }

  .falling-flower {
    position: fixed;
    top: -100px;
    pointer-events: none;
    animation-timing-function: linear;
  }

  /* Animation for falling */
  @keyframes fall {
    to {
      transform: translateY(110vh) rotate(360deg);
      opacity: 0;
    }
  }
</style>
</head>
<body>

<h1>Since you love flowers, these are for you</h1>

<script>
  // SVG for a realistic pink rose with green stem (simplified)
  const roseSVG = `
    <svg width="40" height="60" viewBox="0 0 40 60" xmlns="http://www.w3.org/2000/svg">
      <g>
        <!-- Stem -->
        <rect x="18" y="20" width="4" height="40" fill="#a4c639" rx="1" ry="1" />
        <!-- Petals -->
        <circle cx="20" cy="15" r="12" fill="#ff5ca3" />
        <circle cx="15" cy="10" r="8" fill="#ff8fba" />
        <circle cx="25" cy="10" r="8" fill="#ff8fba" />
        <circle cx="20" cy="5" r="6" fill="#ffbdd7" />
      </g>
    </svg>
  `;

  // SVG for a simple pink petal
  const petalSVG = `
    <svg width="15" height="10" viewBox="0 0 15 10" xmlns="http://www.w3.org/2000/svg">
      <ellipse cx="7.5" cy="5" rx="7" ry="4" fill="#ff79a1" />
    </svg>
  `;

  function createFlower(type) {
    const div = document.createElement('div');
    div.classList.add('falling-flower');
    div.style.left = Math.random() * 100 + 'vw';
    div.style.animationDuration = (5 + Math.random() * 5) + 's';
    div.style.animationName = 'fall';
    div.style.opacity = 1;
    div.style.willChange = 'transform, opacity';

    div.innerHTML = type === 'rose' ? roseSVG : petalSVG;
    div.style.width = type === 'rose' ? '40px' : '15px';
    div.style.height = type === 'rose' ? '60px' : '10px';

    document.body.appendChild(div);

    // Remove after animation ends to avoid clutter
    div.addEventListener('animationend', () => div.remove());
  }

  // Generate flowers continuously
  setInterval(() => {
    const flowerType = Math.random() < 0.3 ? 'rose' : 'petal'; // 30% rose, 70% petal
    createFlower(flowerType);
  }, 300); // every 300ms

</script>

</body>
</html>
