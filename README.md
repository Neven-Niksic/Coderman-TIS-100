# Coderman: TIS-100
A set of puzzle solutions for the video game TIS-100, basically a walkthrough. As visible below, some puzzles received more than one solution.

On Windows, put the .txt files directly into /Documents/My Games/TIS-100/[numbers]/save. If you're using something else, I can't help you. There are also screenshots if you want to make it easier to visualize what the code actually looks like in-game.

## Levels (and their stats)
1. Self-Test Diagnostic (00150.x)
   - .0: 83 cycles, 8 nodes, 8 instructions - 2023-02-13
2. Signal Amplifier (10981.x)
   - .0: 160 cycles, 4 nodes, 6 instructions - 2023-02-13
3. Differential Converter (20176.x)
   - .0: 355 cycles, 6 nodes, 16 instructions - 2023-02-13
   - .1: 395 cycles, 5 nodes, 17 instructions - 2023-02-13
   - .2: 394 cycles, 5 nodes, 16 instructions - 2023-02-13
4. Signal Comparator (21340.x)
   - .0: 327 cycles, 6 nodes, 25 instructions - 2023-02-13
5. Signal Multiplexer (22280.x)
   - .0: 262 cycles, 5 nodes, 16 instructions - 2023-02-13
6. Sequence Generator (30647.x)
   - .0: 132 cycles, 5 nodes, 18 instructions - 2023-02-20
7. Sequence Counter (31904.x)
   - .0: 478 cycles, 5 nodes, 28 instructions - 2023-02-20
8. Signal Edge Detector (32050.x)
   - .0: 390 cycles, 7 nodes, 28 instructions - 2023-02-21
   - .1: 390 cycles, 6 nodes, 25 instructions - 2023-02-21
   - .2: 322 cycles, 7 nodes, 28 instructions - 2023-02-21

## Commentary
1. Self-Test Diagnostic - Literally can't go better than this. Might not be able to go worse either, not without rendering the puzzle unsolvable.
2. Signal Amplifier - Doubling is achieved by storing IN.A into ACC, and then adding the ACC to itself
3. Differential Converter (20176.x) - Three solutions, every one handling the subtractions inside different nodes.
4. Signal Comparator (21340.x) - Two different nodes have to check where to output 1.
5. Signal Multiplexer (22280.x) - Solution lies in simply checking if IN.S is positive, negative, or equal to 0.
6. Sequence Generator (30647.x) - In hindsight, maybe I should have tried using the BAK instead of that one additional node.
7. Sequence Counter (31904.x) - Every time you add a new number, you increase the counter on the right by 1.
8. Signal Edge Detector (32050.x) - First subtraction shows the actual difference. If that is negative, negate it to make it positive. Second subtraction checks if the difference is less than 10. (I came up with this entire solution by thinking of it in reverse.)

## Observations
- JEZ, JNZ, JGZ, and JLZ are effectively combinations of IF and GOTO from real life
- likewise, JMP and JRO are pure GOTO

## Versions
0.1 (2023-02-22) - initial release
- README created
- solutions for the first 8 levels
0.1.1 (2023-02-25)
- touched up the README

## Legal
I wanted to put this under an open license, but didn't know which one to choose because I thought of multiple possible interpretation of what this repo could (legally) be. I ended up going with the "it's technically a walkthrough" interpretation and thus chose CC. It's CC0 because honestly, what more do I need here? Read the LICENSE file for details.
