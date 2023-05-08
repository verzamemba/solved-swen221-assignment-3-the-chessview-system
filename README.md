Download Link: https://assignmentchef.com/product/solved-swen221-assignment-3-the-chessview-system
<br>
<h1>1           Introduction</h1>

The ChessView system is a simple Java application for viewing chess games written in <em>long algebraic chess notation</em>. The following shows a screenshot from ChessView:

ChessView has only one window, which allows the user to move forward and backward through a chess game. The moves of the game, written in long algebraic chess notation, are given in the rightmost pane of the window; the current state of the chess board is shown in the leftmost pane.

<strong>Long Algebraic Notation </strong>Long algebraic chess notation is a way for writing down the moves taken during a chess game. The following illustrates the start of a game in this notation:

<table width="124">

 <tbody>

  <tr>

   <td width="62">White</td>

   <td width="62">Black</td>

  </tr>

  <tr>

   <td width="62">e2-e4</td>

   <td width="62">e7-e5</td>

  </tr>

  <tr>

   <td width="62">d2-d4</td>

   <td width="62">e5xd4</td>

  </tr>

  <tr>

   <td width="62">Nb1-c3</td>

   <td width="62">Qd8-f6</td>

  </tr>

 </tbody>

</table>

The first move by White, e2-e4, indicates the pawn at position e2 will advance to position e4. When indicating pawn movement, no piece specifier is given. However, when indicating the movement of other pieces a specifier is always given. The specifiers are: N=kNight; B=Bishop; R=Rook; Q=Queen; K=King. So, for example, White’s last move above, Nb1-c3, indicates his Knight moves from b1 to

Figure 1: Illustrating the state of a game after 3 rounds.

c3. Finally, a move where one piece takes another is indicated using a x, as in Black’s move e5xd4 — the (black) pawn at position e5 takes the (white) pawn at d4. Figure 1 shows the state of the board after the moves in the above game have been made.

There are a number of other moves which can be made during a game of chess, including: <em>putting a king in check </em>(e.g Qe1-h4+)), <em>castling </em>(e.g. O-O), <em>pawn promotion </em>(e.g. b7-b8=N) and <em>en passant </em>(e.g. b4xa3ep). If you are not familiar with the rules of Chess, the following links provide an excellent starting point:

http://en.wikipedia.org/wiki/Chess http://en.wikipedia.org/wiki/Chess_notation http://en.wikipedia.org/wiki/Algebraic_chess_notation

You can also find many other good resources on the Internet regarding the game of chess.

<strong>NOTE: </strong><em>you do not need to be any good at playing chess in order to complete this assignment</em>.

<h2>Running Chess View</h2>

To get started, download the chessview-buggy.jar file from the lecture schedule on the course website. You will find several example games are provided as well. As usual, you can run the program from the command-line as follows: java -jar chessview-buggy.jar

You should see the ChessView window open up and a chess board being displayed. You should also be able to navigate forward and backward through a game.

Figure 2: Illustrating an example Board object, which contains a 2-dimensional array of pieces. An empty square is indicated by a box with a slash, and this corresponds to the array cell holding null. The first element of the row array, and the first element of each column array are unused (marked in gray). This allows the row numbers to line up with those of the normal chess board. Column a of the chess board corresponds to index 1 in the column array, and so on for columns b, c, …, etc.

<h2>Understanding Chess View</h2>

When you expand or import the chessview jar file, you should find the following java packages:

swen221/assignment2/chessview/ swen221/assignment2/chessview/pieces/ swen221/assignment2/chessview/moves/ swen221/assignment2/tests/

Some notes on these packages:

<ul>

 <li>The swen221/assignment2/chessview/ package contains the high-level game classes, including those for representing the chess board and the game itself.</li>

 <li>The swen221/assignment2/chessview/pieces/ packages contains a class for each of the different chess pieces. These contain code related to the movement of the pieces.</li>

 <li>The swen221/assignment2/chessview/moves/ packages contains a class for each of the different kind of move that can be made in the game. These contain code related to structuring a move, and ensuring it is valid.</li>

 <li>The Main class provides a simple Graphical User Interface for the ChessView system. <strong>NOTE:</strong></li>

</ul>

you do not need to modify or fix any code in this package.

The class swen221/assignment2/chessview/Board is one of the main classes in the ChessView system. This is responsible for representing the state of the chess board, including the position of all of the pieces. This uses a 2-dimensional array to represent the chess board, where each cell in that array represents a location on the board. The board also provides methods for determining whether a particular diagonal, horizontal or vertical move will be unobstructed. Figure 2 provides a visualisation of a simple Board object.

<h1>What to Do</h1>

Currently, there are a number of tests provided for the chess game in the file ChessViewTests. You must add tests to this file with the aim of achieving close to 100% coverage using Emma and, in the process, identify and fix problems in the code. The following illustrates Emma being used in Eclipse:

In this example, we see that the coverage obtained for the class ArraySet is 66.6%.

<strong>HINT: </strong>The purpose of using Emma is to help you find problems in the code base. These problems should be relatively clear (based on the rules of Chess) once you have found them, but have been deliberately obfuscated to make it hard to find them just by looking at the code.

<strong>HINT: </strong>There are <em>at least ten </em>distinct problems that have been planted in the code base. See if you can find them all!

<strong>HINT: </strong>Your submitted code will be marked against a hidden set of test cases which achieves 100% coverage.

<strong>HINT: </strong>The viewer supplied is to help you see the games being played. It is not intended to be tested.