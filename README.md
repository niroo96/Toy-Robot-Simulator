# Toy Robot Simulator
Solution for Toy Robot Simulator in Python

# Challenge
Create a library that can read in commands of the following form:
PLACE X Y DIRECTION
MOVE
LEFT
RIGHT
REPORT

- The library allows for a simulation of a toy robot moving on a 5 x 5 square tabletop.
- There are no obstructions on the table surface.
- The robot is free to roam around the surface of the table, but must be prevented from falling to destruction. Any movement that would result in this must be prevented, however further valid movement commands must still be allowed.
- PLACE will put the toy robot on the table in position X,Y and facing NORTH, SOUTH, EAST or WEST.
- (0,0) can be considered as the SOUTH WEST corner and (4,4) as the NORTH EAST corner.
- The first valid command to the robot is a PLACE command. After that, any sequence of commands may be issued, in any order, including another PLACE command. The library should discard all commands in the sequence until a valid PLACE command has been executed.
- The PLACE command should be discarded if it places the robot outside of the table surface.
- MOVE will move the toy robot one unit forward in the direction it is currently facing.
- LEFT and RIGHT will rotate the robot 90 degrees in the specified direction without changing the position of the robot.
- REPORT will announce the X,Y and orientation of the robot.
- A robot that is not on the table can choose to ignore the MOVE, LEFT, RIGHT and REPORT commands.
- The library should discard all invalid commands and parameters.

Example Input and Output:

a)
PLACE 0 0 NORTH
MOVE
REPORT
Output: 0 1 NORTH

b)
PLACE 0 0 NORTH
LEFT
REPORT
Output: 0 0 WEST

c)
PLACE 1 2 EAST
MOVE
MOVE
LEFT
MOVE
REPORT
Output: 3 3 NORTH

- Use your preferred language, platform and IDE to implement this solution.
- Your solution should be clean and easy to read, maintain and execute.
- There must be a way to supply the library with input data. 
- Writing an interface (command prompt or otherwise) is not mandatory.
- You should provide sufficient evidence that your solution is complete by, as a minimum, indicating that it works correctly against the supplied test data.
- You should provide build scripts or instructions to build and verify the solution.
- The code should be original and you may not use any external libraries or open source code to solve this problem, but you may use external libraries or tools for building or testing purposes.

# Notes
1. classes/robot.py includes the main functions of the Toy Robot Simulator

2. test.py includes the test cases for testing to ensure that the toy robot is placed within the bounds of the 5x5 square top, ensure that the toy robot does not move out of bounds, can do a full left & right turn & 3 example test cases.

3. All test cases including the example test cases supplied have run successfully with no errors and this can be verified by running the test.py file in a python environment.

4. The simulator is run from the main.py python script. Refer to the section below for instructions

# Instructions
1. Run in the main.py file in a python 3.x environment to initial the Toy Robot Challenge Script.

2. Place the toy robot inside the 5x5 square top using the PLACE function in the following format [PLACE {X} {Y} {Direction}]
e.g (PLACE 0 0 NORTH, PLACE 1 2 EAST).

3. Use the MOVE function to move the toy robot one unit forward in the direction it is currently facing.

4. Use the LEFT & RIGHT function to rotate the toy robot 90 degrees in the specified direction without changing the position of the toy robot.

5. Use the REPORT function to announce the X,Y Coordinates & the orientation of the robot.

5. Use the QUIT function to exit the toy robot simulator script.

# Author
Niroo Arjuna
