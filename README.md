<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For Crystal 💌</title>

<style>

/* =========================
   GENERAL
========================= */

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  overflow: hidden;

  display: flex;
  justify-content: center;
  align-items: center;

  padding: 20px;

  font-family: Georgia, "Times New Roman", serif;
  color: #69394b;

  background:
    radial-gradient(
      circle at 15% 20%,
      rgba(255,255,255,.9) 0 2px,
      transparent 3px
    ),
    radial-gradient(
      circle at 75% 30%,
      rgba(255,255,255,.8) 0 2px,
      transparent 3px
    ),
    radial-gradient(
      circle at 40% 80%,
      rgba(255,255,255,.8) 0 2px,
      transparent 3px
    ),
    linear-gradient(
      135deg,
      #ffd6e7,
      #ffeaf2,
      #ffd1df
    );

  background-size:
    180px 180px,
    220px 220px,
    250px 250px,
    cover;
}


/* =========================
   CARD
========================= */

.card {

  width: min(92vw, 520px);
  max-height: 90vh;

  overflow-y: auto;

  text-align: center;

  background: rgba(255,255,255,.84);

  backdrop-filter: blur(15px);
  -webkit-backdrop-filter: blur(15px);

  border: 2px solid rgba(255,255,255,.85);

  border-radius: 30px;

  padding: 38px 28px;

  box-shadow:
    0 25px 70px rgba(128,58,87,.20),
    inset 0 1px 0 rgba(255,255,255,.8);

  animation: appear .8s ease;

  position: relative;
  z-index: 5;
}

.card::-webkit-scrollbar {
  width: 5px;
}

.card::-webkit-scrollbar-thumb {
  background: #e8a2ba;
  border-radius: 10px;
}


/* =========================
   HEART
========================= */

.heart {

  font-size: 55px;

  margin-bottom: 8px;

  animation: heartbeat 1.5s infinite;
}


/* =========================
   HEADINGS
========================= */

h1 {

  font-size: clamp(32px, 9vw, 46px);

  margin: 5px 0 15px;

  color: #c54f7b;
}

p {

  font-size: 18px;

  line-height: 1.6;
}

.question {

  font-size: 21px;

  margin: 22px 0 30px;
}


/* =========================
   BUTTONS
========================= */

.buttons {

  display: flex;

  justify-content: center;

  align-items: center;

  gap: 18px;

  min-height: 60px;

  position: relative;
}

button {

  border: none;

  border-radius: 999px;

  padding: 14px 30px;

  font-size: 17px;

  font-family: inherit;

  cursor: pointer;

  transition:
    transform .25s ease,
    background .25s ease,
    box-shadow .25s ease;
}


/* YES */

#yesBtn {

  background: #d95783;

  color: white;

  box-shadow:
    0 8px 22px rgba(217,87,131,.3);
}

#yesBtn:hover {

  transform: scale(1.08);

  background: #c94673;

  box-shadow:
    0 12px 28px rgba(217,87,131,.4);
}


/* NO */

#noBtn {

  background: #f2dce5;

  color: #8b5368;

  position: relative;

  transition: transform .18s ease;
}


/* =========================
   CALENDAR
========================= */

.calendar-wrapper {

  margin-top: 25px;

  display: flex;

  flex-direction: column;

  gap: 12px;
}

.calendar-wrapper label {

  text-align: left;

  font-size: 16px;

  color: #8b5368;

  font-weight: bold;

  margin-top: 5px;
}


input[type="date"],
select {

  width: 100%;

  padding: 15px;

  border: 2px solid #efb5c9;

  border-radius: 15px;

  background: #fff8fb;

  color: #69394b;

  font-family: inherit;

  font-size: 17px;

  outline: none;

  transition: .25s ease;
}

input[type="date"]:focus,
select:focus {

  border-color: #d95783;

  box-shadow:
    0 0 0 4px rgba(217,87,131,.1);
}


/* CONFIRM */

.confirm {

  margin-top: 8px;

  background: #d95783;

  color: white;

  box-shadow:
    0 8px 20px rgba(217,87,131,.25);
}

.confirm:hover {

  transform: scale(1.05);

  background: #c94673;
}


/* =========================
   LETTER
========================= */

.letter {

  text-align: left;

  background: #fffaf4;

  border-radius: 15px;

  padding: 28px;

  margin-top: 20px;

  box-shadow:
    0 10px 30px rgba(100,50,60,.15),
    inset 0 0 30px rgba(230,180,150,.08);

  position: relative;

  animation: letterOpen 1s ease;
}

.letter::before {

  content: "♥";

  position: absolute;

  top: 10px;

  right: 15px;

  color: #e68aaa;

  font-size: 22px;
}

.letter::after {

  content: "♡";

  position: absolute;

  bottom: 10px;

  left: 15px;

  color: #e68aaa;

  font-size: 20px;
}

.letter h2 {

  text-align: center;

  color: #c54f7b;

  margin-top: 0;

  font-size: 27px;
}

.letter p {

  font-size: 17px;
}

.date-display {

  text-align: center;

  color: #c54f7b;

  font-weight: bold;

  background: #fff0f5;

  padding: 12px;

  border-radius: 12px;
}

.signature {

  text-align: right;

  font-size: 20px;

  margin-top: 25px;

  color: #c54f7b;

  font-style: italic;
}


/* =========================
   HIDDEN
========================= */

.hidden {

  display: none !important;
}


/* =========================
   FLOATING HEARTS
========================= */

.floating-heart {

  position: fixed;

  bottom: -40px;

  pointer-events: none;

  animation: floatUp linear forwards;

  opacity: .75;

  z-index: 1;
}


/* =========================
   SPARKLES
========================= */

.sparkle {

  position: fixed;

  width: 4px;

  height: 4px;

  background: white;

  border-radius: 50%;

  pointer-events: none;

  animation: sparkle 2s ease-in-out infinite;
}


/* =========================
   ANIMATIONS
========================= */

@keyframes heartbeat {

  0%, 100% {
    transform: scale(1);
  }

  50% {
    transform: scale(1.12);
  }
}

@keyframes appear {

  from {

    opacity: 0;

    transform:
      translateY(25px)
      scale(.94);
  }

  to {

    opacity: 1;

    transform:
      translateY(0)
      scale(1);
  }
}

@keyframes letterOpen {

  from {

    opacity: 0;

    transform:
      scale(.85)
      rotate(-2deg);
  }

  to {

    opacity: 1;

    transform:
      scale(1)
      rotate(0);
  }
}

@keyframes floatUp {

  0% {

    transform:
      translateY(0)
      rotate(0deg);

    opacity: .8;
  }

  100% {

    transform:
      translateY(-115vh)
      rotate(360deg);

    opacity: 0;
  }
}

@keyframes sparkle {

  0%, 100% {

    opacity: .2;

    transform: scale(.6);
  }

  50% {

    opacity: 1;

    transform: scale(1.4);
  }
}


/* =========================
   MOBILE
========================= */

@media (max-width: 480px) {

  body {
    padding: 15px;
  }

  .card {

    width: 100%;

    padding: 30px 20px;

    border-radius: 25px;
  }

  .heart {
    font-size: 48px;
  }

  h1 {
    font-size: 34px;
  }

  .question {
    font-size: 19px;
  }

  .buttons {
    gap: 10px;
  }

  button {
    padding: 13px 23px;
    font-size: 16px;
  }

  .letter {
    padding: 22px 20px;
  }

  .letter p {
    font-size: 16px;
  }
}

</style>
</head>


<body>


<!-- =====================================
     QUESTION
===================================== -->

<div class="card" id="questionCard">

  <div class="heart">💗</div>

  <h1>Hi, Crystal!</h1>

  <p class="question">

    I have a little question for you...

    <br><br>

    Would you go on a date with me? 🥺

  </p>


  <div class="buttons">

    <button id="yesBtn">
      Yes 💕
    </button>

    <button id="noBtn">
      No
    </button>

  </div>

</div>



<!-- =====================================
     DATE + PLACE
===================================== -->

<div class="card hidden" id="calendarCard">

  <div class="heart">
    🗓️
  </div>

  <h1>
    Yay! 💗
  </h1>

  <p>

    Pick a date and place, Crystal.

    <br>

    I'll take care of the rest. ♡

  </p>


  <div class="calendar-wrapper">


    <!-- DATE -->

    <label for="datePicker">
      📅 Pick a date
    </label>

    <input
      type="date"
      id="datePicker"
    >


    <!-- PLACE -->

    <label for="placePicker">
      📍 Pick a place
    </label>

    <select id="placePicker">

      <option value="">
        Choose a place...
      </option>

      <option value="Starbucks ☕️">
        Starbucks ☕️
      </option>

      <option value="MOA 🌊">
        MOA 🌊
      </option>

      <option value="Festival Mall 🛍️">
        Festival Mall 🛍️
      </option>

      <option value="SM BF 🏬">
        SM BF 🏬
      </option>

      <option value="SM Sucat 🛒">
        SM Sucat 🛒
      </option>

    </select>


    <!-- CONFIRM -->

    <button
      class="confirm"
      id="confirmBtn"
    >

      Confirm Date 💌

    </button>


  </div>

</div>



<!-- =====================================
     LETTER
===================================== -->

<div class="card hidden" id="letterCard">

  <div class="heart">
    💌
  </div>


  <div class="letter">

    <h2>
      Dear Crystal,
    </h2>


    <p>

      I don't really know the perfect way to say this,
      so I'll just be honest.

    </p>


    <p>

      I really like spending time with you, and I'd love
      to make a little memory together.

    </p>


    <p>

      So when I asked you out, I wasn't just asking
      randomly. I genuinely wanted to spend a day with you.

    </p>


    <p>

      And now that you've picked a date...

      <br>

      I guess it's officially a date. 🥹💕

    </p>


    <!-- CHOSEN DATE + PLACE -->

    <p
      class="date-display"
      id="chosenDate"
    ></p>


    <p>

      I'll be looking forward to it.

      <br>

      Take care until then, okay? ♡

    </p>


    <div class="signature">

      — Shin 💗

    </div>

  </div>

</div>



<script>


/* =====================================
   ELEMENTS
===================================== */

const yesBtn =
  document.getElementById("yesBtn");

const noBtn =
  document.getElementById("noBtn");

const questionCard =
  document.getElementById("questionCard");

const calendarCard =
  document.getElementById("calendarCard");

const letterCard =
  document.getElementById("letterCard");

const confirmBtn =
  document.getElementById("confirmBtn");

const datePicker =
  document.getElementById("datePicker");

const placePicker =
  document.getElementById("placePicker");

const chosenDate =
  document.getElementById("chosenDate");



/* =====================================
   YES BUTTON
===================================== */

yesBtn.addEventListener("click", () => {

  questionCard.classList.add("hidden");

  calendarCard.classList.remove("hidden");

  createHearts(15);

});



/* =====================================
   PLAYFUL NO BUTTON
===================================== */

noBtn.addEventListener(
  "mouseenter",
  moveNoButton
);

noBtn.addEventListener(
  "touchstart",
  (event) => {

    event.preventDefault();

    moveNoButton();

  }
);

noBtn.addEventListener(
  "click",
  moveNoButton
);


function moveNoButton() {

  const buttonRect =
    noBtn.getBoundingClientRect();


  const padding = 20;


  const maxX =
    Math.max(
      80,
      (window.innerWidth -
        buttonRect.width) / 2 -
        padding
    );


  const maxY =
    Math.max(
      80,
      (window.innerHeight -
        buttonRect.height) / 2 -
        padding
    );


  const x =
    Math.random() * maxX * 2 - maxX;


  const y =
    Math.random() * maxY * 2 - maxY;


  noBtn.style.transform =
    `translate(${x}px, ${y}px)`;

}



/* =====================================
   CONFIRM DATE + PLACE
===================================== */

confirmBtn.addEventListener(
  "click",
  () => {


    /* Check date */

    if (!datePicker.value) {

      alert(
        "Pick a date first, Crystal! 🥺💕"
      );

      return;
    }


    /* Check place */

    if (!placePicker.value) {

      alert(
        "Pick a place too! 📍💕"
      );

      return;
    }


    /* Format date */

    const selected =
      new Date(
        datePicker.value +
        "T00:00:00"
      );


    const formattedDate =
      selected.toLocaleDateString(
        "en-US",
        {
          weekday: "long",
          month: "long",
          day: "numeric",
          year: "numeric"
        }
      );


    /* Display date + place */

    chosenDate.innerHTML =

      `📅 Our date:<br>
       ${formattedDate}
       <br><br>
       📍 Our place:<br>
       ${placePicker.value}
       💕`;


    /* Switch screens */

    calendarCard.classList.add(
      "hidden"
    );

    letterCard.classList.remove(
      "hidden"
    );


    /* Celebration */

    createHearts(30);

  }
);



/* =====================================
   FLOATING HEARTS
===================================== */

function createHeart() {

  const heart =
    document.createElement("div");


  heart.className =
    "floating-heart";


  const hearts = [
    "💗",
    "💕",
    "💖",
    "💘",
    "💝",
    "♡"
  ];


  heart.textContent =
    hearts[
      Math.floor(
        Math.random() *
        hearts.length
      )
    ];


  heart.style.left =
    Math.random() * 100 + "vw";


  heart.style.fontSize =
    (16 +
      Math.random() * 22) +
    "px";


  heart.style.animationDuration =
    (4 +
      Math.random() * 4) +
    "s";


  document.body.appendChild(
    heart
  );


  setTimeout(
    () => heart.remove(),
    8000
  );

}



function createHearts(amount) {

  for (
    let i = 0;
    i < amount;
    i++
  ) {

    setTimeout(
      () => createHeart(),
      i * 120
    );

  }

}



/* Background hearts */

setInterval(
  () => createHeart(),
  1400
);



/* =====================================
   SPARKLES
===================================== */

function createSparkle() {

  const sparkle =
    document.createElement("div");


  sparkle.className =
    "sparkle";


  sparkle.style.left =
    Math.random() * 100 + "vw";


  sparkle.style.top =
    Math.random() * 100 + "vh";


  sparkle.style.animationDelay =
    Math.random() * 2 + "s";


  document.body.appendChild(
    sparkle
  );


  setTimeout(
    () => sparkle.remove(),
    4000
  );

}


setInterval(
  () => createSparkle(),
  900
);



/* =====================================
   PREVENT PAST DATES
===================================== */

const today =
  new Date();


const yyyy =
  today.getFullYear();


const mm =
  String(
    today.getMonth() + 1
  ).padStart(2, "0");


const dd =
  String(
    today.getDate()
  ).padStart(2, "0");


datePicker.min =
  `${yyyy}-${mm}-${dd}`;


</script>

</body>
</html>
