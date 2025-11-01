# Order it

## 

## Order it

### Problem Description

Chef Alex meticulously documented the sequential instructions for a new recipe, ensuring optimal culinary outcomes through systematic organization. However, during a busy period in the kitchen, the list became disorganized. As the instructions are now out of sequence, Alex requires assistance to restore them to their proper order.

The list may be corrected solely by removing a contiguous segment of instructions and reinserting it at any other location within the list. Each cut-and-insert operation incurs a fixed cost of one unit.

Determine the minimum number of cut-and-insert operations required to restore the shuffled list of instructions to their original sequence.

### Constraints

1\<= N \<= 10

### Input

First line contains a single integer N representing the number of instructions in the list

Next line contains the word "shuffled"

Next N lines contain strings including spaces representing the instruction

Next line contains the word "original"

Next N lines contain string including spaces representing an instruction

### Output

Single Integer which represents the minimum cost to rearrange.

### Time Limit (secs)

1

### Examples

Example 1

Input

5

shuffled

Whisk the onion

Bake the butter

Season the garlic

Fold the flour

Fold the lettuce

original

Fold the flour

Whisk the onion

Bake the butter

Fold the lettuce

Season the garlic

Output

2

Explanation

From the input you can see the 5 instructions. The two operations on the shuffled instruction list will result on the original instruction list

* Cut and insert instruction "Fold the flour" to the top of list.  
* Cut and insert instruction "Fold the lettuce" above "Season the garlic"

The above is one of the ways to rearrange lists in 2 operations which is the minimum.

Example 2

Input

6

shuffled

Dice the onion

Dice the rice

Pour the onion

Stir the egg

Fold the lettuce

Serve the tomato

original

Pour the onion

Stir the egg

Fold the lettuce

Dice the onion

Dice the rice

Serve the tomato

Output

1

Explanation

From the input you can see the 6 instructions.

* Cut the instructions "Dice The onion" and "Dice the Rice" together and insert it above "Serve the tomato" instructions which results in original instruction list.

With 1 operation the list can be rearranged and that is the minimum.

# Cable Wrap

## Cable Wrap

### Problem Description

In a design lab, the floor is modelled as a 2D square grid of size N × M. An iron rod, represented by 'R', is fixed to the floor. A cable, represented by 'C', is laid over the grid and may weave above or below this rod.

A typical top view of the grid with rod and cable is shown below.

* where'R' \- represents a rod fixed to the floor.  
* 'C' \- represents a cable laid over or under the rods.  
* '.' \- represents empty space.

The rods are always placed horizontally or vertically between edges of the grid. The cable starts and ends at the edges of the grid but never starts or ends on the same cell as a rod.

Adjacent cable cells are always connected horizontally or vertically (never diagonally). Cables do not run side by side \- there will always be at least one empty cell gap between two separate cable paths. Similarly, cables do not run directly adjacent to rods. Also, cables can't run over the rods and vice versa, only intersection is allowed.

When the cable overlaps a rod:

* If the rod passes above the cable, the cell is marked as 'R'.  
* If the cable passes above the rod, the cell is marked as 'C'.

You have a special power that allows you to switch the positions of the rod and cable at any cell:

* If the rod is above the cable, you can switch to make the cable go above the rod.  
* If the cable is above the rod, you can switch to make the rod go above the cable.

Your goal is to determine the minimum number of such switches required to unwrap the cable completely \- meaning it can be freely pulled holding both ends without getting caught around any rod.

### Constraints

4 \<= N, M \<= 20

### Input

The first line contains two integers, N and M, separated by a space, which denote the number of rows and columns of the floor grid.  
Each of the next N lines has M characters: '.' for an empty cell, 'C' for cable, and 'R' for rod, separated by spaces.

### Output

Single integer representing minimum number of times power needs to be used to unwrap the cable.

### Time Limit (secs)

1

### Examples

Example 1

Input

5 5

..R..

CCCCC

..R.C

CCRCC

..R..

Output

1

Explanation

The image provided in the *Problem Description* section corresponds to this input. There are two cells where the special power may be applied. Utilizing the special power on either cell is sufficient to release the cable. Assuming the special power is used at the cell located in row 2, column 3 (using 1-based indexing), this action elevates the rod to the top position, thereby unwrapping and fully freeing the cable.

Example 2

Input

5 11

CCC.CCC.CCC

C.C.C.C.C.C

CRCRCRRRCRR

C.C.C.C.C.C

C.CCC.CCC.C

Output

2

Explanation

The below image depicts the above input.

The image demonstrates that the special power may be applied to the rod cells positioned in columns 7 and 11\. Activation at these specific locations elevates the cable above the rods, effectively removing any obstructions.

Example 3

Input

7 6

CCCRCC

...R.C

CCCCCC

C..R..

CCCCCC

...R.C

CCCRCC

Ouput

0

Explanation

The below image depicts the above input.

In this scenario, no power is required, as the cable is not coiled around the rod and can be easily removed by holding both ends and pulling them simultaneously.

# Gravity Glide

## Gravity Glide

### Problem Description

Aarav is learning programming by creating fun simulations. One day, he decides to build a game where a ball drops onto a 2D grid filled with diagonal slides.

Aarav's game involves a ball that drops onto a grid. The grid contains several diagonal slides, each placed randomly and tilted at a 45-degree angle. When the ball is dropped from a starting point, it will slide along a slope if it lands on one; otherwise, gravity pulls it straight down.

Aarav starts with a certain amount of energy. For every unit of distance the ball slides, it uses 1 unit of energy. If the ball gets stuck between two slides, it can unlock itself by spending energy equal to the product of its current x-coordinate and y-coordinate. Once unlocked, the ball continues sliding along any available slide, still using 1 unit of energy per unit distance.

The ball keeps moving until it either reaches the ground (x \= 0\) or runs out of energy and gets stuck. Slides may touch but never cross each other, creating complex paths where the ball can change direction. No two slides are collinear. From any given point, the ball will always have only one possible direction to move.

### Constraints

1 \<= number of sliders \<= 50

0 \<= x, y coordinates \<= 50

The inputs will always ensure that from the given point, the ball will have only one possible direction to move.

If the ball is on the slide, it should be considered on the outer side, not the inner side. Outer side is the side facing top of the grid.

### Input

The first line contains an integer N, the number of slides.

The next N lines each contain four space-separated integers, representing the starting and ending points of each slide.

The last line contains three space-separated integers: the starting x and y coordinates of the ball, and its initial energy.

### Output

Print the final position (x, y) where the ball lands.

### Time Limit (secs)

1

### Examples

Example 1

Input

8

2 4 5 1

1 3 3 1

2 5 5 8

4 5 6 3

1 10 3 8

4 10 6 12

1 14 3 12

3 6 1 8

5 15 21

Output

2 4

Explanation

The given input is visualized below.

The black lines indicate sliders while the red dot is the position from where the ball is dropped.

* The ball starts at (5, 15\) with 21 units of energy.  
* It falls to (5, 11\) due to gravity, then slides one unit (energy left: 20).  
* Gravity pulls it to (4, 7), then it slides to (3, 6\) (energy left: 19).  
* At (3, 6), the ball is stuck. To unlock, it spends 18 energy (3 × 6), leaving 1 unit.  
* With 1 unit energy left, it slides to (2, 5), then gravity pulls it to (2, 4), where it stops. Hence (2, 4\) is the final position of the ball.

Example 2

Input

7

1 1 3 3

4 1 6 3

4 5 5 6

2 5 4 3

2 2 0 4

5 2 7 0

5 6 7 4

2 7 5

Output

4 0

Explanation

The given input is visualized below.

The black lines indicate sliders while the red dot is the position from where the ball is dropped.

* The ball starts at (2, 7\) with 5 units of energy.  
* Gravity pulls it to (2, 5), then it slides to (4, 3\) (energy left: 3).  
* Gravity pulls it to (4, 1), then to (4, 0), where it stops.

# Zoobin

## Zoobin

### Problem Description

The city zoo is currently undergoing significant renovations. To improve both visitor experience and animal welfare, the zookeeping staff have opted to reorganize certain animal habitats.

The zoo is organized as a network of enclosures connected by designated paths, with no additional space available. Animals cannot be swapped between enclosures because they would disrupt each other if they used the same path. To resolve this, the zookeeper developed a rotational strategy known as the "zoobin approach," where all animals are moved simultaneously to their subsequent locations. This method ensures that each animal arrives at its intended enclosure without crossing paths or creating confusion.

For example, consider,

Assume the nodes \[1 to 5\] as enclosures and edges connecting them as path. zoobin approach involves moving the animals from enclosures1 to 3, 3 to 4, 4 to 2 and 2 to 1 simultaneously. A single rotation is made to achieve this.

Now given the initial layout of the zoo and an expected layout, find the minimum such rotation required to move the animals to their expected places.

### Constraints

Number of simple loops present \* E \<= 50

### Input

First Line consist of Integer E representing the total path connecting enclosures

Next E lines will contain two integers A and B separated by space representing the paths between enclosure A and B, of current layout

Next E lines will contain two integers A and B separated by space representing the paths between enclosure A and B, of Expected layout

### Output

Single integer representing minimum rotation required to achieve the expected layout

### Time Limit (secs)

1

### Examples

Example 1

Input

6

1 2

1 3

1 5

3 4

4 5

2 4

1 2

1 4

1 5

2 3

3 4

3 5

Output

2

Explanation

Assume the zoo layout as the left one below. Initially we will make the round move on 1,2,4 and 5 loop. The resultant layout will be the middle layout below. Next, we will make the move on 1,5,3 and 2 loop resulting in the right layout which is the resultant layout.

Thus 2 rotations are needed, that's the minimum hence print the same.

Example2

Input

7

5 6

6 1

5 4

3 4

2 3

1 2

5 7

1 2

1 6

2 3

2 7

3 4

4 5

5 6

Output

3

Explanation

The layout below on left represents the given input. Moving animals on the outer layer results 3 times will result in the expected layout on right.

# Box Game

## Box Game

### Problem Description

Dev, a Rubik's Cube whiz who specializes in solving just one side, challenges his brother Ved with a tricky twist.

The Challenge:

Dev scrambles a Rubik's Cube and gives Ved a set of instructions to solve *one* specific face. But there is a catch\! Dev might have secretly changed the colour of one cube unit, making the cube slightly faulty. To make things even harder, he also includes one extra, incorrect instruction in the list.

Ved must now figure out:

1. Is the cube faulty? Did Dev change a cube's colour?  
2. Identify the wrong instruction. Which step in the instructions will lead to failure if followed?

Can you help Ved solve this Rubik's Cube puzzle with a twist?

The Rubik Cube schematics are described below

Faces of the cubes are described according to the numbers.

1 \- base, 2 \- back, 3 \- top, 4 \- front, 5 \- left, 6 \- right.

Rules:

1\. 'turn left' \- front goes to left, left goes to back, back goes to right, right goes to front, top side will be rotated right, whereas base side will be rotated left.

2\. 'turn right' \- front goes to right, right goes to back, back goes to left, left goes to front, top side will be rotated left, whereas base side will be rotated right.

3\. 'rotate front' \- front goes to base, base goes to back, back goes to top, top goes to front, left side will be rotated right, whereas right side will be rotated left.

4\. 'rotate back' \- front goes to top, top goes to back, back goes to base, base goes to front, left side will be rotated left, whereas right side will be rotated right.

5\. 'rotate left' \- top goes to left, left goes to base, base goes to right, right goes to top, front side will be rotated left, whereas back side will be rotated right.

6\. 'rotate right' \- top goes to right, right goes to base, base goes to left, left goes to top, front side will be rotated right, whereas back side will be rotated left.

7\. '\<side\> \<row/col\> \<direction\>' \- this will turn the row/column (1-indexed) of the side '\<side\>' in the given direction '\<direction\>'. E.g. If the instruction is 'top 1 left', this states that the 1st row of the top side will be turned towards left. If the instruction is 'top 1 down', this states that the 1st column of the top side will be turned downwards. (The direction is specified by imagining the specific side in the front of the eye level, then the row/column is turned).

You are given the initial faces of the cube (visualize it being placed in front at eye level), and the instructions that Dev had given to Ved (instructions comprises of the rules described above). The faces may have multiple colours defined by various alphabets.

Note: There is no guarantee that the colour which is faulty will be the one which will be completed after executing the instructions.

### Constraints

3 \<= N \<= 15

2 \<= K \<= 101

Colours on each side of the box consists of upper-case English alphabets only.

### Input

First line consists of 2 space separated integers \- N & K (where '*N'* is the number of rows and columns on each side of the face and '*K*' is the number of instructions Dev provided to Ved)

Next 6\*N lines, each N lines describes each face of the cube in the order described above with each line consisting of N space separated characters.

Next 'K' lines describe the instructions the cube will perform.

1. Line 1: N K Two space-separated integers:  
   1. N: The number of rows and columns on each side of the Rubik's Cube face.  
   2. K: The number of instructions Dev provides to Ved.  
2. Next 6N lines: Each of these lines represents a face of the cube, described as follows:  
   1. Line Format: N space-separated characters (representing the colours on that face).  
   2. Order: The faces are described in this order: Base, Back, Top, Front, Left, Right.  
3. Last K lines: Each line describes an instruction Dev gives Ved, where each instruction might involve rotating a specific face's column/row (e.g., "right 2 up" means rotate the 2nd column of right face upwards).

### Output

"Faulty" (If and only if the cube is faulty, without quotes)

\<extra\_instruction\>

OR

"Not Possible" (If after executing instructions, the side of the cube is unsolved, without quotes)

### Time Limit (secs)

1

### Examples

Example 1

Input

3 4

W R G

G R B

W R B

Y Y W

W G R

R B R

O G O

O O O

O O O

G W G

Y B W

R Y R

B B Y

G W B

G W B

W Y B

G Y R

Y O Y

back 2 down

front 3 right

front 1 up

back 2 up

Output

front 1 up

Explanation

The required rotations of the cube to solve one side are described in the pictures above. The third instruction (front 1 up) is the extra instruction which leads one side of the cube unsolved. Also, the cube is not faulty, therefore, the answer is: "front 1 up"

Example 2

Input

3 6

W O O

G W G

R R B

G O R

B R W

O W G

Y W W

Y Y W

Y Y O

R R Y

B O Y

R G Y

G G B

B G R

W R B

G G O

B B O

B O W

front 3 up

turn left

front 3 down

top 2 down

left 2 right

top 3 up

Output

Faulty

top 2 down

Explanation

From the images above, one unit of 'Y' color is manipulated with one unit of 'G' color. After correcting the manipulation and executing the instructions, we can say that the instruction 'top 2 down' is an extra instruction causing one side of the cube being unsolved. Therefore, the answer is:

Faulty

top 2 down

Example 3

Input

3 2

O O Y

G G R

R B Y

W Y B

B Y W

B W G

W B R

G B R

G G W

R R O

G W O

B Y O

O O Y

O O Y

W W Y

G W B

B R R

G Y R

base 1 right

top 2 left

Output

Not Possible

Explanation

It can be analyzed the cube is not faulty and executing any of the instructions does not lead to solve one of the sides. Therefore, the answer is: "Not Possible"

# Solve The Expression

## Solve The Expression

### Problem Description

Neena, a third-year engineering student, is enthusiastic about the competitive programming and often participates in the intercollegiate technical fests to test her problem-solving skills. On one occasion, she is presented with a complex problem that necessitates the evaluation of a mathematical expression incorporating bitwise operations and brackets, with the understanding that brackets take precedence in the order of operations.

In this task, numerals (0-9), bitwise operators, and brackets are represented as 7-segment display patterns. The entire expression is presented in this format. The objective is to convert the 7-segment representations into binary strings, evaluate the resulting expression, and return the final numerical result.

Note: The standard configuration for a 7-segment display within a 3x3 matrix, where all LEDs are illuminated, is shown below. Please refer to the following representation:
Figure 1: All LEDs illuminated, depicted 3x3 structure

The question requires that the following steps be taken to arrive at a solution:

1. Convert the 7-segment representation into binary strings:  
   * Each number or operator is represented in a 3x3 seven-segment format.  
   * Read the pattern from left-to-right and top-to-bottom, assigning:  
     * 1 for a segment that is ON.  
     * 0 for a segment that is OFF.  
   * This forms the binary representation of the given symbol.  
   * Let us see another digit represented in LED as well as its corresponding binary format
]Figure 2: LED denoting the digit 2

* For multi-digit numbers, concatenate the binary representations of each digit from left to right.  
1. Evaluate the expression:  
* Apply the bitwise operations according to the following precedence order (highest to lowest) \-  
  * Brackets \- ( )  
  * Logical NOT  
  * Logical OR  
  * Logical AND

Ascertain the outcome: Upon completing the evaluation, provide the numerical value by aligning the resulting string with the initial numerical format.

Note:

The 7-segment patterns corresponding to digits, operators, and brackets are not standardised and Will differ from testcase to testcase.

### Constraints

1 \<= N \<= 32 (where, N denotes total of operands, operators, and brackets in the expression)

The expression is always valid and will have a valid answer.

### Input

First three line contains 7-segment representation of numbers from 0-9.

Next three lines contains 7-segment representation of operators and brackets in the order \- Logical OR, Logical AND, Logical NOT, Opening bracket, Closing bracket.

Last three lines contains the 7-segment representation of the expression.

### Output

Numeric value which denotes the result of the expression

### Time Limit (secs)

1

### Examples

Example 1

Input

 \_     \_  \_     \_  \_  \_  \_  \_ 

| |  | \_| \_||\_||\_ |\_   ||\_||\_|

|\_|  ||\_  \_|  | \_||\_|  ||\_| \_|

 \_        \_  \_ 

| || ||\_||    |

| ||\_|| ||\_  \_|

 \_        \_    

|\_ |\_|| ||\_|  |

|\_|  ||\_| \_|  |

Output

51

Explanation

The input is as follows:

The required expression to be solve is: 64 && 91

where '&&'is Logical AND

The binary representation of 64 will be: 010110111000111001

The binary representation of 91 will be: 010111011000001001

When we perform Logical AND with both binary strings, we will get binary string as: 010110011000001001, which gives numeric value as 51

Hence the answer, 51\.

Example 2

Input

 \_           \_     \_  \_  \_  \_ 

| |  || ||\_|| || |  |  | \_||\_|

|\_|  || || || ||\_| \_|  |  |  |

 \_        \_  \_ 

|\_||\_ |\_ |\_  \_|

|\_|  ||\_||\_  \_|

 \_     \_     \_  \_  \_       

|\_   ||\_|| ||\_|  | \_||\_ | |

|\_   ||\_|| ||\_|  | \_|  || |

Output

2

Explanation

The input is as follows:

The required expression to solve is: (1 || 2 || 7\) && 2

where '||' is Logical OR and '&&' is Logical AND

The binary representation for 1 will be: 000001001

The binary representation for 2 will be: 000101101

The binary representation for 7 will be: 010001001

Upon solving the expression according to the precedence, we get answer 2\.
