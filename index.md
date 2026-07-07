# Floor Cleaning Robot
A robot that cleans up the floor for me because I hate cleaning my room! We have a roomba at my house, and it has been extremely helpful. So, I thought making my own to personally use for my room would be great to have. It will be able to move and also detect objects to maneuver around them.

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Siwoo L. | Mitty | Electrical Engineering | Rising junior

<img width="472" height="530" alt="Screenshot 2026-06-29 at 2 21 28 PM" src="https://github.com/user-attachments/assets/f5d4005c-0bb8-4d6e-a374-850f16c7ec4e" />

<img width="678" height="501" alt="Screenshot 2026-07-07 at 3 59 54 PM" src="https://github.com/user-attachments/assets/7a027018-a5ef-4a4f-9b64-004608bcf3b6" />

<!--  
# Final Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

My final milestone was adding modifications. I added several new changes beyond the base robot, one of them being a remote control. The remote control doesn't allow you to explicitly control the robot, but it does allow you to stop the car and move it backwards. It also has a button to initiate self driving. Basically, the self driving is the code from the previous milestone, allowing the car to turn when it sees obstacles and continue moving forward. It is automatic, and doesn't require you to control the robot. Additionally, when the car is told to stop, it will also play a buzzer sound to let the user know it has stopped moving. Another button makes it move in reverse until it is told to stop. These options were added because I originally wanted a way for the robot to let the user know when it is done cleaning. So, I decided the best way is for the user to tell the robot when to stop themselves. This way, it still allows the robot the be automatic while also allowing the user to stop the car when they are personally satisfied with the job. It also allows for a bit more maneuverability with the reverse function. 

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE
-->


# Second Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/XC_h1YrTGfY?si=G6Vd2hrbpergPy9Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my second milestone, I decided to make the code for the robot to move. This includes moving forward, backwards, left, and right. This will be important since the entire point of the project is for the car to be able to move so it can clean the floor. It will also be able to do more complex movements, such as avoiding obstacles by using sensors. The ultrasonic module can detect objects in front of it, and the car will move out of the way if there is something 2 to 10 cm in front of it. There are also sensors on the side of the car. This allows it to move out of the way if there is an obstacle on the side that the front sensor can't detect. However, there were several difficulties. Sometimes, the robot wouldn't go forward or turn properly. To fix this, I had to adjust the exterior. The vacuum cleaner was too heavy, so it weighed down the car. I taped a caster wheel onto the back of the vacuum. This allowed it to be slightly elavated above the ground so it doesn't cause friction. Additionally, I changed the speed of one of the wheels so that it doesn't swerve off to the side. Overall, the code seems to be working very well. The robot moves properly with little swerving. And when it detects an obstacle, it maneuvers out of the way properly. My next steps are going to be adding modifications. One modification I plan to add is a buzzer so that it can play a sound when the robot finishes cleaning.

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/Skr94AJwVgE?si=Ho1cachBUrD_6yUX" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my first milestone, I wanted to complete the exterior and design of the robot and also do the wiring. The components include wheels, an arduino board, a battery, breadboards, a vacuum, an ultrasonic sensor, and some other important items. The wheels and motor are what allow the robot to maneuver. The arduino board is used to mount the code and get the robot to move. The battery powers the system. The ultrasonic sensor will allow the robot to detect obstacles in front of it, and provide real time data so it can adjust and maneuver around the obstruction. There were several difficulties in the construction of the robot. There were instructions in order to build it, which was simple enough; however, there were no instructions for attaching the vacuum cleaner to the robot. To solve this, I removed the small breadboard and replaced it with a full sized breadboard. I attached the vacuum to one end of the breadboard, and planned to attach the other end to the robot so the vacuum sticks out in front of the robot. However, this led to a few other complications. First off, the vacuum cleaner was too big and tall for the robot, so the breadboard wouldn't be able to stick to the robot. So, I got another small breadboard and simply attached that to the robot first. Then I attached the full sized breadboard on top of the small one. Another issue was attaching the ultrasonic module. Because the circuits in breadboards are only connected across each row, the ultrasonic module would not be able to be pointed straight. So, I took the small breadboard from before and stuck on top of the edge of the full sized breadboard. I put it perpendicular to the full sized breadboard so the I could point the ultrasonic sensor forward while keeping the pins up and down a column. Overall, the design of the car works perfectly and all the wires are connected to the proper places. My next step is coding the robot so that it can move properly.

# Starter

<iframe width="560" height="315" src="https://www.youtube.com/embed/qBhGqpVJxa8?si=h7hAl-xQ921PcBfY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

As a starter project, I chose the retro arcade console. Some essential components include buttons, LED dot matrix modules, and a digitron display. The buttons turn on the device as well as controlling the games. The LED dot matrix module serves as the screen, and the digitron display serves as the scoreboard. Through this project, I learned how to solder properly and what mistakes to avoid while doing it.


# Schematics 
<img width="985" height="546" alt="Screenshot 2026-07-07 at 3 59 45 PM" src="https://github.com/user-attachments/assets/b2034f05-db6f-4fb8-8353-87cdda3bd3c2" />


# Code
```c++
#include <EEPROM.h>
#include <IRremote.h>
#include <Wire.h>
#include <MPU6050_light.h> // Ensure "MPU6050_light" by rfetick is installed via Library Manager

MPU6050 mpu(Wire);

const int IR_RECEIVE_PIN = 12;  // Define the pin number for the IR Sensor
const int BUZZER_PIN = 11;      // Define the pin for the buzzer

float leftOffset = 1.0;
float rightOffset = 1.0;

// Gyroscope tracking variables
float targetAngle = 0;
float kp = 7.0;        // Proportional gain (handles immediate drift)
float ki = 0.3;        // Integral gain (eliminates persistent veering/steady-state error)
float integralE = 0;   // Accumulates error over time to force the car straight

const int A_1B = 5;
const int A_1A = 6;
const int B_1B = 9;
const int B_1A = 10;

const int trigPin = 3;
const int echoPin = 4;

const int rightIR = 7;
const int leftIR = 8;

// State variable
bool isSelfDriving = false; 

// Function prototype declarations
String decodeKeyValue(long result);
float readSensorData();
void moveForwardGyro(int baseSpeed); // Uses Gyro to drive straight
void moveBackward(int speed);
void stopMove();
void backLeft(int speed);
void backRight(int speed);
void playFinishedSound(); 

void setup() {
  Serial.begin(9600);
  Wire.begin();

  // Motor pins configuration
  pinMode(A_1B, OUTPUT);
  pinMode(A_1A, OUTPUT);
  pinMode(B_1B, OUTPUT);
  pinMode(B_1A, OUTPUT);

  pinMode(leftIR, INPUT);
  pinMode(rightIR, INPUT);
  
  // Buzzer configuration
  pinMode(BUZZER_PIN, OUTPUT); 

  // --- HARDWARE CALIBRATION ---
  // Ex: If your car naturally veers right, your left motor might be stronger.
  EEPROM.write(0, 100); // left motor offset percentage (0 to 100)
  EEPROM.write(1, 100); // right motor offset percentage (0 to 100)

  // Ultrasonic sensor configuration
  pinMode(echoPin, INPUT);
  pinMode(trigPin, OUTPUT);
  leftOffset = EEPROM.read(0) * 0.01;
  rightOffset = EEPROM.read(1) * 0.01;

  // Initialize Gyroscope
  Serial.println("CALIBRATING GYRO. KEEP CAR PERFECTLY STILL...");
  byte mpuStatus = mpu.begin();
  if(mpuStatus != 0) {
    Serial.println("Could not connect to MPU6050!");
    while(1); // Freeze if gyro is missing/miswired
  }
  delay(1000);
  mpu.calcOffsets(); // Calibrates baseline offsets (car must be static here)
  Serial.println("GYRO CALIBRATED & READY");

  // Initialize IR remote receiver
  IrReceiver.begin(IR_RECEIVE_PIN, ENABLE_LED_FEEDBACK); 
  Serial.println("REMOTE CONTROL START");
}

void loop() {
  // Read gyro orientation on every loop cycle
  mpu.update();

  // 1. CHECK FOR IR REMOTE COMMANDS FIRST
  if (IrReceiver.decode()) {
    String key = decodeKeyValue(IrReceiver.decodedIRData.command);
    
    if (key != "ERROR") {
      Serial.println(key);

      if (key == "1") {
        isSelfDriving = true;  // Activate self-driving
        targetAngle = mpu.getAngleZ(); // Lock in current direction as "straight ahead"
        integralE = 0;                 // Clear any leftover accumulated error
        Serial.println("Self-Driving: ON");
      } 
      else if (key == "2") {
        isSelfDriving = false; // Deactivate self-driving
        stopMove();            // Instantly stop the car
        Serial.println("Self-Driving: OFF (STOPPED)");
        playFinishedSound();   // Play the completion chime and reset IR
      }
      else if (key == "3") {
        isSelfDriving = false;
        stopMove();
        delay(500);
        moveBackward(150);
      }
    }
    IrReceiver.resume();  // Enable receiving of the next value
  }

  // 2. EXECUTE SELF-DRIVING LOGIC (ONLY IF ACTIVATED)
  if (isSelfDriving) {
    float distance = readSensorData();
    int leftSide = digitalRead(leftIR);   // 0: Obstructed  1: Empty
    int rightSide = digitalRead(rightIR);

    // Ultrasonic sensor detects obstacle ahead
    if (distance >= 1.00 && distance <= 10.00) {
      stopMove();
      delay(200);
      backRight(255);   // Turns RIGHT at max power to clear obstacle faster
      delay(600);       
      
      // Stop and let chassis settle before locking new direction
      stopMove();
      delay(150);
      targetAngle = mpu.getAngleZ(); 
      integralE = 0;    // Reset error accumulator for the new straight line path
    } 
    // Front path clear, check sides
    else {
      if (!leftSide && rightSide) {
        // If left blocked turn left
        backLeft(255);
        delay(400);
        
        stopMove();
        delay(150);
        targetAngle = mpu.getAngleZ();
        integralE = 0;
      } 
      else if (leftSide && !rightSide) {
        // If right blocked turn right
        backRight(255);
        delay(400);
        
        stopMove();
        delay(150);
        targetAngle = mpu.getAngleZ();
        integralE = 0;
      } 
      else if (!leftSide && !rightSide) {
        // If both sides blocked back up
        moveBackward(150);
        delay(500);
        
        stopMove();
        delay(150);
        targetAngle = mpu.getAngleZ();
        integralE = 0;
      } 
      // If everything clear, move straight using gyro correction
      else {
        moveForwardGyro(150);
      }
    } 
  }
}

// Gyroscope-assisted Forward Movement (PI Control)
void moveForwardGyro(int baseSpeed) {
  float currentAngle = mpu.getAngleZ();
  float error = targetAngle - currentAngle; // Calculate angular drift

  // Accumulate error over time to combat steady-state veering
  integralE += error;
  
  // Constrain integral to prevent "windup" (runaway runaway speed corrections)
  integralE = constrain(integralE, -50.0, 50.0); 

  // Combined P (immediate) and I (time-based) correction
  // Note: If car spins uncontrollably out of a straight line, remove the negative signs below
  int correction = int((-error * kp) + (-integralE * ki)); 

  // Apply correction adjustments to baseline wheel speeds
  int leftSpeed = baseSpeed + correction;
  int rightSpeed = baseSpeed - correction;

  // Clamp constraints so PWM stays within valid limits (0 to 255)
  leftSpeed = constrain(leftSpeed, 0, 255);
  rightSpeed = constrain(rightSpeed, 0, 255);

  // Drive H-bridge motors
  analogWrite(A_1B, 0);
  analogWrite(A_1A, int(leftSpeed * leftOffset));
  analogWrite(B_1B, int(rightSpeed * rightOffset));
  analogWrite(B_1A, 0);
}

// Function for buzzer when stopped moving
void playFinishedSound() {
  tone(BUZZER_PIN, 300, 150); 
  delay(200);
  tone(BUZZER_PIN, 350, 150); 
  delay(200);
  tone(BUZZER_PIN, 400, 400); 
  delay(450);

  noTone(BUZZER_PIN); // Relinquish timer hardware back to the system
  
  // Re-initialize the IR receiver so it continues to work after the buzzer sounds
  IrReceiver.begin(IR_RECEIVE_PIN, ENABLE_LED_FEEDBACK); 
  Serial.println("IR Receiver Reset & Ready");
}

// Function to read the ultrasonic distance sensor
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
  analogWrite(A_1B, speed); // Left motor backwards
  analogWrite(A_1A, 0);
  analogWrite(B_1B, speed); // Right motor forwards
  analogWrite(B_1A, 0);
}

void backRight(int speed) {
  analogWrite(A_1B, 0);     // Left motor forwards
  analogWrite(A_1A, speed);
  analogWrite(B_1B, 0);     // Right motor backwards
  analogWrite(B_1A, speed);
}

// Map the hexadecimal codes to remote button names
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
| MPU6050 Gyroscope | A sensor that measures orientation and angular velocity | $6.99 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/(https://www.amazon.com/ATmega328P-Arduino-Compatible-Arduino-Voltage-Compatible/dp/B0FMR3NRHH/ref=sxin_20_pa_sp_search_thematic_sspa?content-id=amzn1.sym.292df443-b323-44ae-8b40-9a666975b8b5%3Aamzn1.sym.292df443-b323-44ae-8b40-9a666975b8b5&crid=3SWISGYHLYM17&cv_ct_cx=arduino+uno+r3&keywords=arduino+uno+r3&pd_rd_i=B0FMR3NRHH&pd_rd_r=34bf79ca-c4b5-4fa3-93e9-8bb64feb9be7&pd_rd_w=3tK7P&pd_rd_wg=tYdwl&pf_rd_p=292df443-b323-44ae-8b40-9a666975b8b5&pf_rd_r=G0TJM6X8J4E47J2GZNBE&qid=1782776935&s=electronics&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D&sprefix=arduino+uno+r3%2Celectronics%2C142&sr=1-3-6024b2a3-78e4-4fed-8fed-e1613be3bcce-spons&aref=EBJyi2Mu5B&sp_csd=d2lkZ2V0TmFtZT1zcF9zZWFyY2hfdGhlbWF0aWM&psc=1"> Link </a> |

# Other Resources/Examples

- https://docs.sunfounder.com/projects/3in1-kit-v2/en/latest/car_project/car_assemble.html
- https://smitra123.github.io/Saagnik-Mitra-s-BSE-Portfolio/
