let months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"];
let populations = [];

function setup() {
  createCanvas(600, 400);
  for (let i = 0; i < months.length; i++) {
    populations.push(random(500000, 10000000)); // Fake population data
  }
}

function draw() {
  background(220);
  for (let i = 0; i < months.length; i++) {
    let barHeight = map(populations[i], 500000, 10000000, 50, 300);
    fill(100, 150, 255);
    rect(i * 50 + 50, height - barHeight, 40, barHeight);
  }
}
