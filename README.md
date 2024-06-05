# Knight-Tour-Solver
A Knight's Tour is a sequence of moves of a knight on a chessboard such that the knight visits every square exactly once. The knight moves in an L-shape: two squares in one direction and then one square perpendicular, or one square in one direction and two squares perpendicular. The tour can start from any square on the board. A closed tour returns to the starting square, while an open tour does not.
## Implementation
Warnsdorff's rule is a heuristic used to find a Knight's Tour on a chessboard. The rule suggests that the knight should always move to the square with the fewest onward moves, i.e., the square from which the knight will have the least number of potential future moves. By doing this, the knight avoids getting stuck in positions where no further moves are possible, which is crucial for completing the tour.
Caching helps in implementing Warnsdorff's rule by storing the results of computations that would otherwise need to be recalculated multiple times. For example, caching is used to store the number of onward moves for each square on the board. When the knight is determining its next move, it can quickly access the precomputed values instead of recalculating them, thus speeding up the decision-making process. This is especially useful in larger boards where the computational load can become significant.
## Usage
1. Ensure installation of any g++ compiler and C++11 at least.
2. Clone the repo or download 
3. Run `compile-mac.sh` to compile the source code into an executable inside ./bin
4. Run `./bin/knights-tour.bin [x] [y] [width] [height]` where `x`, `y` are starting positions, and `width`, `height` represent size.
5. If a solution is found, it will be logged inside of the directory under `Tour Solution <width>x<height>.txt`.
