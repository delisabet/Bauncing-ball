Bauncing-ball
===========
//starting position
float xpos = random(30, width -30) ; 
float ypos= random(30, height -30) ; 
//speed of the ball
float xspeed = 2; 
float yspeed = 2.1;

int xdirection = 1;
int ydirection = 1;


void setup() {
  size (600, 600);
  frameRate (30); 
}

void draw () 
{
  background(#66CDCD); 
  drawEllipse(xpos, ypos, 200);
  drawEllipse(xpos*3, ypos, 30);

  xpos = xpos + ( xspeed * xdirection );
  ypos = ypos + ( yspeed * ydirection );
  
  // Test to see if the shape exceeds the boundaries of the screen
  // If it does, reverse its direction by multiplying by -1
  if (xpos > width-30 || xpos < 30) {
    xdirection *= -1;
  }
  if (ypos > height-30 || ypos < 30) {
    ydirection *= -1;
  }

 
}

void drawEllipse(float x, float y, float g) {
// float x/y etc to make variables on the draw//
  ellipse (x, y, 60, 60); 
  noStroke ();
  fill(0, g, 0); 
} 

09/26/12
