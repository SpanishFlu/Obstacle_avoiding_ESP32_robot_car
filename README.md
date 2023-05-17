# Obstacle_avoiding_ESP32_robot_car
This program creates a robot that can avoid obstacles by using an ultrasonic sensor, a DC motor, and an ESP32 microprocessor. The robot may be made to go forward, backward, right, or left, halt the motors, and ramp up the speed of the motors gradually so as not to overcharge the batteries. The robot utilizes a servo motor to scan the right and left for impediments before choosing the path with the longest turning radius. The program also has a feature that uses the ultrasonic sensor to determine how far away the closest obstacle is.

The pin mappings for the servo motor, DC motors, and ultrasonic sensor are first defined in the programme. The servo motor is installed and positioned in the centre while the pin modes are configured during setup. After giving the ultrasonic sensor some time to settle, the initial distance is read by repeatedly using the readPing function.

The readPing function is used in the loop function to read the distance to the closest obstacle. The robot pauses and rotates to check for obstructions to the right and left using the lookRight and lookLeft functions if the distance is less than or equal to 15 cm. Then, using the turnRight or turnLeft function, the robot makes a turn in the direction with the greatest distance. The robot uses the moveForward function to move forward if the separation is larger than 15 cm.

The DC motors are managed using the moveForward, moveBackward, turnRight, turnLeft, and moveStop functions. The moveForward, moveBackward, turnRight, and turnLeft functions each call the rampUpSpeed function to progressively increase the motors' speed.

Overall, using an ESP32 microcontroller, an ultrasonic sensor, and DC motors, this programme gives the fundamental building blocks for an obstacle-avoiding robot. However, more features and functionality may need to be added to the programme depending on the particular needs of the robot and the environment in which it operates.
