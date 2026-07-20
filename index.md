# Floor Cleaning Robot
A robot that cleans up the floor for me because I hate cleaning my room! We have a roomba at my house, and it has been extremely helpful. So, I thought making my own to personally use for my room would be great to have. It will be able to move and also detect objects to maneuver around them.

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Siwoo L. | Mitty | Electrical Engineering | Rising junior

<img width="472" height="530" alt="Screenshot 2026-06-29 at 2 21 28 PM" src="https://github.com/user-attachments/assets/f5d4005c-0bb8-4d6e-a374-850f16c7ec4e" />

<img width="678" height="501" alt="Screenshot 2026-07-07 at 3 59 54 PM" src="https://github.com/user-attachments/assets/7a027018-a5ef-4a4f-9b64-004608bcf3b6" />

<!--  
# Modifications

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

My final milestone was adding modifications. I added several new changes beyond the base robot, one of them being a remote control. The remote control doesn't allow you to explicitly control the robot, but it does allow you to stop the car and move it backwards. It also has a button to initiate self driving. Basically, the self driving is the code from the previous milestone, allowing the car to turn when it sees obstacles and continue moving forward. It is automatic, and doesn't require you to control the robot. Additionally, when the car is told to stop, it will also play a buzzer sound to let the user know it has stopped moving. Another button makes it move in reverse until it is told to stop. These options were added because I originally wanted a way for the robot to let the user know when it is done cleaning. So, I decided the best way is for the user to tell the robot when to stop themselves. This way, it still allows the robot the be automatic while also allowing the user to stop the car when they are personally satisfied with the job. It also allows for a bit more maneuverability with the reverse function. I also added a gyroscope. I mounted it onto the breadboard and wired it into the arduino. Afterwards, I programmed it so that the car could move in a straight line. There were several issues with this however. Sometimes, the car still moved off to the side or even stopped entirely. To fix this, I had to replace the battery. I also had to increase the correction strength of the gyroscope. After making these changes, when the car veers a bit to one direction, the gyroscope will realign the car so that it goes back into a straight line. This was a helpful addition to the car since it would always swerve to one side. 

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE
-->

# Final Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/egsT9s4-E2g?si=jijALDdNPPh8MfX2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

My final milestone was adding an IR receiver so that the car can take commands from a remote control. The remote control allows the user to control the robot. Clicking the button one makes the robot initiate a self drive function. Basically, it will move forward and turn to avoid obstacles, essentially driving by itself. However, the remote control also allows the user to directly control the robot. By clicking the button 2, the robot will stop moving and stay completely still until further instructions are given. Button 3 puts the car in reverse, making it go backwards. Button 4 and 6 makes the car turn left and right, respectively. Before, the robot would automatically move by itself as soon as the power was turned on. There was no way to stop the robot until the power was removed. Additionally, if the robot got stuck, there would be no way for the user to  free the robot unless they physically removed it from its surroundings. Now, with this remote control, the user has more control and maneuverability with the car. For my next steps, I plan on adding several modifications. First off, I will add two LEDs, a green one and a red one. The green one will light up when the robot goes forward, while the red one will light up when the car backs up. I also plan on adding a buzzer to let the user know when the robot is done cleaning. Additionally, I want to add a gyroscope. One issue with my current robot is that it does not move straight and will drift to one side. By using a gyroscope, the car will be able to adjust its position and realign itself so that it goes straight.


# Second Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/XC_h1YrTGfY?si=G6Vd2hrbpergPy9Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my second milestone, I decided to make the code for the robot to move. This includes moving forward, backwards, left, and right. This will be important since the entire point of the project is for the car to be able to move so it can clean the floor. It will also be able to do more complex movements, such as avoiding obstacles by using sensors. The ultrasonic module can detect objects in front of it, and the car will move out of the way if there is something 2 to 10 cm in front of it. There are also sensors on the side of the car. This allows it to move out of the way if there is an obstacle on the side that the front sensor can't detect. However, there were several difficulties. Sometimes, the robot wouldn't go forward or turn properly. To fix this, I had to adjust the exterior. The vacuum cleaner was too heavy, so it weighed down the car. I taped a caster wheel onto the back of the vacuum. This allowed it to be slightly elavated above the ground so it doesn't cause friction. Additionally, I changed the speed of one of the wheels so that it doesn't swerve off to the side. Overall, the code seems to be working very well. The robot moves properly with little swerving. And when it detects an obstacle, it maneuvers out of the way properly. My next step is going to be adding an IR receiver. That way, it can take commands from a remote control and move based on what commands the user gives it.


# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/Skr94AJwVgE?si=Ho1cachBUrD_6yUX" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my first milestone, I wanted to complete the exterior and design of the robot and also do the wiring. The components include wheels, an arduino board, a battery, breadboards, a vacuum, an ultrasonic sensor, and some other important items. The wheels and motor are what allow the robot to maneuver. The arduino board is used to mount the code and get the robot to move. The battery powers the system. The ultrasonic sensor will allow the robot to detect obstacles in front of it, and provide real time data so it can adjust and maneuver around the obstruction. There were several difficulties in the construction of the robot. There were instructions in order to build it, which was simple enough; however, there were no instructions for attaching the vacuum cleaner to the robot. To solve this, I removed the small breadboard and replaced it with a full sized breadboard. I attached the vacuum to one end of the breadboard, and planned to attach the other end to the robot so the vacuum sticks out in front of the robot. However, this led to a few other complications. First off, the vacuum cleaner was too big and tall for the robot, so the breadboard wouldn't be able to stick to the robot. So, I got another small breadboard and simply attached that to the robot first. Then I attached the full sized breadboard on top of the small one. Another issue was attaching the ultrasonic module. Because the circuits in breadboards are only connected across each row, the ultrasonic module would not be able to be pointed straight. So, I took the small breadboard from before and stuck on top of the edge of the full sized breadboard. I put it perpendicular to the full sized breadboard so the I could point the ultrasonic sensor forward while keeping the pins up and down a column. Overall, the design of the car works perfectly and all the wires are connected to the proper places. My next step is coding the robot so that it can move properly.

# Starter

<iframe width="560" height="315" src="https://www.youtube.com/embed/qBhGqpVJxa8?si=h7hAl-xQ921PcBfY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

As a starter project, I chose the retro arcade console. Some essential components include buttons, LED dot matrix modules, and a digitron display. The buttons turn on the device as well as controlling the games. The LED dot matrix module serves as the screen, and the digitron display serves as the scoreboard. Through this project, I learned how to solder properly and what mistakes to avoid while doing it.


# Schematics 
<img width="746" height="424" alt="Screenshot 2026-07-14 at 4 16 19 PM" src="https://github.com/user-attachments/assets/c778bb26-241c-414e-90d1-a205299b11f2" />


# Code
```c++
#include <EEPROM.h>
#include <IRremote.h>
#include <Wire.h>
#include <MPU6050_light.h> 

MPU6050 mpu(Wire);

const int IR_RECEIVE_PIN = 12;  
const int BUZZER_PIN = 11;      // Custom non-blocking buzzer to avoid timer conflicts

float leftOffset = 1.0;
float rightOffset = 1.0;

// --- TUNED FOR FRESH BATTERIES ---
float targetAngle = 0;
float kp = 4.0;        // Bumped up to give the gyro more correction strength
float ki = 0.15;       // Re-enabled a small amount to eliminate the steady left pull
float integralE = 0;  

const int A_1B = 5;
const int A_1A = 6;
const int B_1B = 9;
const int B_1A = 10;

const int trigPin = 3;
const int echoPin = 4;

const int rightIR = 7;
const int leftIR = 8;

bool isSelfDriving = false; 

// Function prototypes
String decodeKeyValue(long result);
float readSensorData();
void moveForwardGyro(int baseSpeed); 
void moveBackward(int speed);
void stopMove();
void backLeft(int speed);
void backRight(int speed);
void playFinishedSoundNonBlocking(); 

void setup() {
  Serial.begin(9600);
  Wire.begin();

  pinMode(A_1B, OUTPUT);
  pinMode(A_1A, OUTPUT);
  pinMode(B_1B, OUTPUT);
  pinMode(B_1A, OUTPUT);

  pinMode(leftIR, INPUT);
  pinMode(rightIR, INPUT);
  
  pinMode(BUZZER_PIN, OUTPUT); 

  // --- MOTOR POWER BALANCE CALIBRATION ---
  // Default equal power:
  EEPROM.write(0, 100); // Left motor power (0 to 100%)
  EEPROM.write(1, 100); // Right motor power (0 to 100%)
  
  // NOTE: If your car hooks hard RIGHT immediately on takeoff, uncomment these:
  // EEPROM.write(0, 85);  // Throttle down the stronger left motor
  // EEPROM.write(1, 100);

  // NOTE: If your car hooks hard LEFT immediately on takeoff, uncomment these:
  // EEPROM.write(0, 100);
  // EEPROM.write(1, 85);   // Throttle down the stronger right motor

  pinMode(echoPin, INPUT);
  pinMode(trigPin, OUTPUT);
  leftOffset = EEPROM.read(0) * 0.01;
  rightOffset = EEPROM.read(1) * 0.01;

  Serial.println("CALIBRATING GYRO. KEEP CAR PERFECTLY STILL...");
  byte mpuStatus = mpu.begin();
  if(mpuStatus != 0) {
    Serial.println("Could not connect to MPU6050!");
    while(1); 
  }
  delay(1000);
  mpu.calcOffsets(); 
  Serial.println("GYRO CALIBRATED & READY");

  IrReceiver.begin(IR_RECEIVE_PIN, ENABLE_LED_FEEDBACK); 
  Serial.println("REMOTE CONTROL START");
}

void loop() {
  // Constantly update the gyro so it tracks angles during operations
  mpu.update();

  // 1. IR REMOTE HANDLING
  if (IrReceiver.decode()) {
    String key = decodeKeyValue(IrReceiver.decodedIRData.command);
    
    if (key != "ERROR") {
      Serial.println(key);

      if (key == "1") {
        isSelfDriving = true;  
        targetAngle = mpu.getAngleZ(); 
        integralE = 0;                 
        Serial.println("Self-Driving: ON");
      } 
      else if (key == "2") {
        isSelfDriving = false; 
        stopMove();            
        Serial.println("Self-Driving: OFF (STOPPED)");
        playFinishedSoundNonBlocking();   
      }
      else if (key == "3") {
        isSelfDriving = false;
        stopMove();
        delay(500);
        moveBackward(150);
      }
    }
    IrReceiver.resume();  
  }

  // 2. SELF-DRIVING NAVIGATION
  if (isSelfDriving) {
    float distance = readSensorData();
    int leftSide = digitalRead(leftIR);   
    int rightSide = digitalRead(rightIR);

    if (distance >= 1.00 && distance <= 10.00) {
      stopMove();
      delay(200);
      backRight(255);   
      
      // Keep updating gyro orientation during execution pauses
      unsigned long turnStart = millis();
      while(millis() - turnStart < 600) { mpu.update(); }
      
      stopMove();
      delay(150);
      mpu.update();
      targetAngle = mpu.getAngleZ(); 
      integralE = 0;    
    } 
    else {
      if (!leftSide && rightSide) {
        backLeft(255);
        unsigned long turnStart = millis();
        while(millis() - turnStart < 400) { mpu.update(); }
        
        stopMove();
        delay(150);
        mpu.update();
        targetAngle = mpu.getAngleZ();
        integralE = 0;
      } 
      else if (leftSide && !rightSide) {
        backRight(255);
        unsigned long turnStart = millis();
        while(millis() - turnStart < 400) { mpu.update(); }
        
        stopMove();
        delay(150);
        mpu.update();
        targetAngle = mpu.getAngleZ();
        integralE = 0;
      } 
      else if (!leftSide && !rightSide) {
        moveBackward(150);
        unsigned long turnStart = millis();
        while(millis() - turnStart < 500) { mpu.update(); }
        
        stopMove();
        delay(150);
        mpu.update();
        targetAngle = mpu.getAngleZ();
        integralE = 0;
      } 
      else {
        // Safe baseline speed for high voltage batteries
        moveForwardGyro(130); 
      }
    } 
  }
}

void moveForwardGyro(int baseSpeed) {
  float currentAngle = mpu.getAngleZ();
  float error = targetAngle - currentAngle; 

  integralE += error;
  integralE = constrain(integralE, -50.0, 50.0); 

  // Smooth PI correction output
  int correction = int((-error * kp) + (-integralE * ki)); 

  int leftSpeed = baseSpeed + correction;
  int rightSpeed = baseSpeed - correction;

  leftSpeed = constrain(leftSpeed, 0, 255);
  rightSpeed = constrain(rightSpeed, 0, 255);

  analogWrite(A_1B, 0);
  analogWrite(A_1A, int(leftSpeed * leftOffset));
  analogWrite(B_1B, int(rightSpeed * rightOffset));
  analogWrite(B_1A, 0);
}

// Bypasses standard hardware Timer 2 conflicts with IRremote
void playFinishedSoundNonBlocking() {
  int notes[] = {300, 350, 400};
  int durations[] = {150, 150, 400};
  
  for (int n = 0; n < 3; n++) {
    long delayValue = 1000000 / notes[n] / 2; 
    long numCycles = notes[n] * durations[n] / 1000; 
    
    for (long i = 0; i < numCycles; i++) {
      digitalWrite(BUZZER_PIN, HIGH);
      delayMicroseconds(delayValue);
      digitalWrite(BUZZER_PIN, LOW);
      delayMicroseconds(delayValue);
    }
    delay(200); 
  }
}

float readSensorData() {
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  float distance = pulseIn(echoPin, HIGH) / 58.00; 
  return distance;
}

void moveBackward(int speed) {
  analogWrite(A_1B, int(speed * leftOffset));
  analogWrite(A_1A, 0);
  analogWrite(B_1B, 0);
  analogWrite(B_1A, int(speed * rightOffset));
}

void stopMove() {
  analogWrite(A_1B, 0);
  analogWrite(A_1A, 0);
  analogWrite(B_1B, 0);
  analogWrite(B_1A, 0);
}

void backLeft(int speed) {
  analogWrite(A_1B, speed); 
  analogWrite(A_1A, 0);
  analogWrite(B_1B, speed); 
  analogWrite(B_1A, 0);
}

void backRight(int speed) {
  analogWrite(A_1B, 0);     
  analogWrite(A_1A, speed);
  analogWrite(B_1B, 0);     
  analogWrite(B_1A, speed);
}

String decodeKeyValue(long result) {
  switch(result){
    case 0x16: return "0";
    case 0xC:  return "1"; 
    case 0x18: return "2"; 
    case 0x5E: return "3"; 
    case 0x8:  return "4"; 
    case 0x1C: return "5"; 
    case 0x5A: return "6"; 
    case 0x42: return "7"; 
    case 0x52: return "8"; 
    case 0x4A: return "9"; 
    case 0x9:  return "+"; 
    case 0x15: return "-"; 
    case 0x7:  return "EQ"; 
    case 0xD:  return "U/SD";
    case 0x19: return "CYCLE";         
    case 0x44: return "PLAY/PAUSE";   
    case 0x43: return "FORWARD";   
    case 0x40: return "BACKWARD";   
    case 0x45: return "POWER";   
    case 0x47: return "MUTE";   
    case 0x46: return "MODE";       
    case 0x0:  return "ERROR";   
    default :  return "ERROR";
  }
}
```

# Bill of Materials
| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| SunFounder 3 in 1 Starter Kit | Contains all the materials in order to create the chasis of the robot | $69.99 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/SunFounder-Ultimate-Tutorials-Beginners-Enthusiasts/dp/B0CGJ235XN/ref=sr_1_2_sspa?crid=1MF6TR1QVOLHY&dib=eyJ2IjoiMSJ9.D9LrCZJnua_keVMLJz2FWvrsniUV2B9R7DGc6wRYHz6Otpv8Utt8-__xGv1lwx9nojGY1Nf7yRZCQD83P9dNdDCT05nniwjjmOwJbx1fITkhe2Gv3KP6mgmDPUreSxmWru_gLtN4TpkL-OP8RawJc6rvWF5XYZ7Yyz8ClkhYe_9iYJjz7jCp31s_YRQ1l3HYETyUsmyyK_92n9jImO7EkfAdnRnrohBF7ArvHUxc85L8vcmJaAij8Cyuemr0kEIC2Cai0IfXb1S6hstdtj73azqfaLjIeBnJ3QxzUSMHnFo.e-MTEgeg1j3FLcFQS6ti5iwHFFl6AIHPrsoVEknDbkE&dib_tag=se&keywords=sunfounder+3+in+1&qid=1782776628&s=electronics&sprefix=sunfounder+3+in+1%2Celectronics%2C137&sr=1-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1"> Link </a> |

| 9V Battery | Powers the entire car | $9.79 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/Amazon-Basics-Performance-All-Purpose-Batteries/dp/B0774D64LT/ref=sr_1_8?crid=3NMAAJ1EWYX44&dib=eyJ2IjoiMSJ9.UTIEEJxrXzAacW7rXzP5baUO2v4AozDKVKm1_F2qlZEkyEEF0ZIysVzSQC4YcYQF4ysud-40LkjJpuJKcnmvJcy0NPpbD8hQHhtvpxKoV_t1Ti55gnWZKsqsGL9k1x7SmKZBupbniMX-5gmulUpidnoXmafRdFEQ-zSb-2f-jJ9mkn0lCEHf4YB4L9aN_pqGGKqpVX1VCILW9ksB_n0qvf27tljxQBzNIbA-aFJ-FJ-3XOcpd7mY9wjTLANV1pyXl83qypWk_y4eHrdE0lr_z8i-HXUX13P9befwoYewP-0.zJouV9mMIeULuZ8gmW00SO3WdYaovoqzNejCJbEKe3Y&dib_tag=se&keywords=9V%2Bbattery&qid=1782776782&s=electronics&sprefix=9v%2Bbattery%2Celectronics%2C192&sr=1-8&th=1"> Link </a> |

| Arduino UNO R3 | A microcontroller that reads physical inputs and controls outputs | $9.99 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/ATmega328P-Arduino-Compatible-Arduino-Voltage-Compatible/dp/B0FMR3NRHH/ref=sxin_20_pa_sp_search_thematic_sspa?content-id=amzn1.sym.292df443-b323-44ae-8b40-9a666975b8b5%3Aamzn1.sym.292df443-b323-44ae-8b40-9a666975b8b5&crid=3SWISGYHLYM17&cv_ct_cx=arduino+uno+r3&keywords=arduino+uno+r3&pd_rd_i=B0FMR3NRHH&pd_rd_r=34bf79ca-c4b5-4fa3-93e9-8bb64feb9be7&pd_rd_w=3tK7P&pd_rd_wg=tYdwl&pf_rd_p=292df443-b323-44ae-8b40-9a666975b8b5&pf_rd_r=G0TJM6X8J4E47J2GZNBE&qid=1782776935&s=electronics&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D&sprefix=arduino+uno+r3%2Celectronics%2C142&sr=1-3-6024b2a3-78e4-4fed-8fed-e1613be3bcce-spons&aref=EBJyi2Mu5B&sp_csd=d2lkZ2V0TmFtZT1zcF9zZWFyY2hfdGhlbWF0aWM&psc=1"> Link </a> |

| MPU6050 Gyroscope | A sensor that measures orientation and angular velocity | $6.99 | [<a href="https://www.amazon.com/HiLetgo-MPU-6050-Accelerometer-Gyroscope-Converter/dp/B01DK83ZYQ/ref=sr_1_5?dib=eyJ2IjoiMSJ9.D75LAmktNfzc3v0s7tjJnKvbplLUBlX900JU-X3C0s-PASA2X4TO93CZ51VTc2Aaf1mcUGMH0P1eNt_f0uzfXDcN6-uqKstxlossZLSlhUePxEFhja-ghso23KE3lPBl8VWRSHdVaYQ56r_99GPI8eT5pYHHFkqWzRX6bhBEldiJz3cmnjXKdF4-_DmPCEhvZdaVlAu3gfOMEYNz5RSEgA0a2ifG4p4rPr6qOY57k4w.ccmkmLaTZYMsCeQceMCs3nrLiHp1smabGOxJMxqjrcc&dib_tag=se&keywords=mpu6050&qid=1783466135&sr=8-5&th=1"> Link </a> |

# Other Resources/Examples

- <a href="https://docs.sunfounder.com/projects/3in1-kit-v2/en/latest/car_project/car_assemble.html"> SunFounder 3in1 </a>
- <a href="https://smitra123.github.io/Saagnik-Mitra-s-BSE-Portfolio/"> Bluestamp Project Guide </a>
