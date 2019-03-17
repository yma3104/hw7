var chime;

var sounds = [];

function preload() {
  soundFormats('m4a');
  for (var i = 0; i < 10; i++) {
    let sound = loadSound('glockenspiel.m4a');
    sound.rate(0.5 * pow(2, i / 5)); // 12-semitone exponential scale

    sounds.push(sound);
  }
}

function setup() {
  createCanvas(600, 400);
  rectMode(CENTER);
}

function draw() {
  background(400);
  noFill();

  for (var i = 0; i < sounds.length; i++) {
    let sound = sounds[i];
    if (sound.isPlaying()) {
      var q = map(sound.currentTime(), 0, sound.duration(), 50, 10);
      for (var x = 10; x < q; x = x + 2) {
      ellipse(width / sounds. length * (i + 1), 200, x + 20);
      }
    }
  }
}

function mouseMoved() {
  if (mouseX < 40 && mouseX > 0) {
    sounds[0].play();
  }
  if (mouseX < 80 && mouseX > 40) {
    sounds[1].play();
  }
  if (mouseX < 120 && mouseX > 80) {
    sounds[2].play();
  }
  if (mouseX < 160 && mouseX > 120) {
    sounds[3].play();
  }
  if (mouseX < 200 && mouseX > 160) {
    sounds[4].play();
  }
  if (mouseX < 240 && mouseX > 200) {
    sounds[5].play();
  }
  if (mouseX < 280 && mouseX > 200) {
    sounds[6].play();
  }
  if (mouseX < 320 && mouseX > 280) {
    sounds[7].play();
  }
  if (mouseX < 360 && mouseX > 320) {
    sounds[8].play();
  }
  if (mouseX < 400 && mouseX > 360) {
    sounds[8].play();
  }
}
