# Barrel-Shifter
Module Explanation 

Inputs:
- In [7:0]: 8-bit input data to be shifted.

- n [2:0]: 3-bit value indicating the number of positions to shift.

- Lr: Direction control signal (1 for left shift, 0 for right shift).

Output:
- Out [7:0]: 8-bit output after shifting.

Functionality (Using always@(*) block):
- If Lr is 1 → Left shift (<<) by n bits
- If Lr is 0 → Right shift (>>) by n bits

Key Points:
- The shifts are logical shifts (not arithmetic), meaning:

- Left shifts (<<) fill zeros from the right.

- Right shifts (>>) fill zeros from the left.

- The always@(*) block ensures that the output updates whenever an input changes (combinational logic).

- reg is used for Out since it’s assigned inside an always block.

