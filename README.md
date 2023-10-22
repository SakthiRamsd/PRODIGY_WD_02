Using HTML, CSS, Javascript to Build the Stopwatch.

HTML file :

    <p class="time">
        <span id="minutes">00</span> :
        <span id="seconds">00</span> :
        <span id="tens">00</span>
      </p>


CSS file :

body {
    width: 100%;
    height: 100vh;
    background-image: url('https://c4.wallpaperflare.com/wallpaper/832/718/324/watch-desk-stopwatch-wallpaper-preview.jpg');
    background-position: center;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }


  Javascript file :

const startTimer = () => {
      tens++;
      if (tens <= 9) {
        appendTens.innerHTML = '0' + tens;
      }
      if (tens > 9) {
        appendTens.innerHTML = tens;
      }

      if (tens > 99) {
        seconds++;
        appendSeconds.innerHTML = '0' + seconds;
        tens = 0;
        appendTens.innerHTML = '0' + 0;
      }

      if (seconds > 9) {
        appendSeconds.innerHTML = seconds;
      }

      if (seconds > 59) {
        minutes++;
        appendMinutes.innerHTML = '0' + minutes;
        seconds = 0;
        appendSeconds.innerHTML = '0' + 0;
      }
    };

