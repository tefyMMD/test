[style.css](https://github.com/user-attachments/files/25094534/style.css)
[indxe.html](https://github.com/user-attachments/files/25094535/indxe.html)[scrips.js](https://github.com/user-attachments/files/25094536/scrips.js)
[scrips.js](https://github.com/user-attachments/files/25094608/scrips.js)
const wrapper = document.getElementById("wrapper");
const question = document.getElementById("question");
const gif = document.getElementById("gif");
const yesBtn = document.getElementById("yes-btn");
const noBtn = document.getElementById("no-btn");[style.css](https://github.com/user-attachments/files/25094609/style.css)@import url('https://fonts.googleapis.com/css2?family=Comic+Relief:wght@400;700&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: whitesmoke;
    font-family:  "Comic Relief", system-ui;;
  }
  
  #gif {
    height: 100%;
    width: 100%;
      cursor: zoom-in;
  }
  
  #gif:active {
      transform: scale3d(1.3,1.3,1.3);
  }
  
  h2 {
    text-align: center;
    font-size: 1.5em;
    color: #e94d58;
    margin: 15px 0;
  }
  #btn-group {
    width: 100%;
    height: 50px;
    display: flex;
    justify-content: center;
    margin-top: 50px;
  }
  button {
    position: absolute;
    width: 150px;
    height: inherit;
    color: white;
    font-size: 1.2em;
    border-radius: 30px;
    outline: none;
    cursor: pointer;
    box-shadow: 0 2px 4px gray;
    border: 2px solid #e94d58;
    font-size: 1.2em;
  }
  button:nth-child(1) {
    margin-left: -200px;
    background: #e94d58;
  }
  button:nth-child(2) {
    margin-right: -200px;
    background: white;
    color: #e94d58;
  }
  
  #no-btn {
    cursor: not-allowed;
  }


yesBtn.addEventListener("click", () => {
  question.innerHTML = "I knew it 😍";
  gif.src = "https://media.giphy.com/media/UMon0fuimoAN9ueUNP/giphy.gif";
});

noBtn.addEventListener("mouseover", () => {
  const noBtnRect = noBtn.getBoundingClientRect();
  const maxX = window.innerWidth - noBtnRect.width;
  const maxY = window.innerHeight - noBtnRect.height;

  const randomX = Math.floor(Math.random() * maxX);
  const randomY = Math.floor(Math.random() * maxY);

  noBtn.style.left = randomX + "px";
  noBtn.style.top = randomY + "px";
});
