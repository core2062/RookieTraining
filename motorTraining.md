# Welcome back to CORE 2062 Rookie Training. Today we are covering motors.  

### Please keep this file open as you progress through the lesson.  

> Motors are components on the robot which turn via electromagnets.   

We use `TalonSRX` to  control motors. 

 1. Please open [Github](https://github.com/core2062/RookieTraining) and clone the files:  

- **RookieTrainingBaseProject.cpp**  
- **RookieTrainingBaseProject.h**   
 Into the **Motor** folder of your repository

 3. Rename "**RookieTrainingBaseProject.cpp**" and "**RookieTrainingBaseProject.h**" to "**[Your name]MotorsProject.cpp**" and "**[Your name]MotorsProject.h**"  

 4. In the end of the private section of the class in "**[your name]MotorsProject.h**" write the following line of code:  

        TalonSRX m_motorTest;  
    This initiates a variable called "**m_motorTest**" of type `TalonSRX`, variables of this type must be made for each motor used in a robot subsystem. 
5. Above the please write the following above the previous line in"**[your name]MotorsProject.h**":

        #define TEST_MOTOR_PORT X
    Where X is a number your intrustor will give you based on the device you are using. This line defines the port of a `talonSRX` on the robot you are using and stores it in a varible for later use.

6. At the beggining of "**[your name]MotorsProject.cpp**"place the following:

        m_motorTest(TEST_MOTOR_PORT)
    This line connects our varible to the real talon allowing us to control the motor that is connected.

7. In the function "**teleopInit**" please write the following:

        m_motorTest.Set(ControlMode::PercentOutput, 0);

    This causes the talon to Initiate control from the code.

8. In the function teleop write:

        m_motorTest.Set(ControlMode::PercentOutput, 0.75);

    This line is used to control the motor taking inputs from -1 to 1 and accepts varibles and operations.

## Thank you for completing the motor lesson please commit and inform the instructor that you are done.
