
  html, body, #area, #sky {
  width: 100%;
  height: 100%;
  margin: 0px;
  padding: 0px;
}

p {
  font-size: 120px;
}

#area {
  animation: fade 20s;
  animation-fill-mode: forwards;
  animation-play-state: running;
  opacity: 1.0;
}

@keyframes fade {
    0% {opacity: 1.0;}
    100% {opacity: 0.0;}
}

#runner {
  background-image: url('https://lh3.googleusercontent.com/-gdMnrXBLlhY/VOpid9p3FcI/AAAAAAAAB-Y/1AN-7Rbw-o0/w426-h511/running%2Bcorriendo.gif');
  background-repeat: no-repeat;
  background-size: 100%;
  height: 200px;
  width: 150px;
  bottom: 10px;
  left: 0px;
  position: absolute;
  transform: rotate(30deg);
  animation: run 2s ease-in;
  animation-fill-mode: forwards;
  //animation-play-state: paused;
}

@keyframes run {
    0% {left: 0%;} 
    100% {left: 42%;}
}

#ball {
  background-image: url('http://media.giphy.com/media/6CiIHzivbQmPu/giphy.gif');
  background-repeat: no-repeat;
  background-size: 100%;
  height: 80px;
  width: 80px;
  bottom: 0px;
  right: 50%;
  position: absolute;
  z-index: 1000;
  animation: kicked 2s, bounce 1s 2 ease-in 0s alternate;
  animation-fill-mode: forwards;
  animation-play-state: paused;
}

@keyframes kicked {
    0% {right: 50%;}
    100% {right: 150px;}
}

@keyframes bounce {
    from {bottom: 30px;} 
    to {bottom: 100px;}
}

#sky {
  background-image: url('http://pre09.deviantart.net/627b/th/pre/f/2013/350/f/7/animation__the_clouds_and_the_sky_by_coralarts-d6y5r9k.png');
  background-repeat: no-repeat;
  background-size: 100% 50%;
  transform: rotate(-0.5deg);
  top: -8px;
  height: 50%;
  width: 100%;
  position: absolute;
}

#goal {
  background-image: url('http://www.clker.com/cliparts/F/D/w/Z/V/P/soccer-goal-hi.png');
  background-repeat: no-repeat;
  background-size: 100%;
  height: 200px;
  width: 300px;
  bottom: -15px;
  right: 20px;
  position: absolute;
}