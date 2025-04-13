# Checkers / Tic-Tac-Toe 5x5

A **Checkers / Tic-Tac-Toe 5x5** game implemented as a **Java Panama Project** with **JNI (Java Native Interface)**.

The game logic is implemented in **C++**, while the graphical interface is built using **Java Swing**. The design follows the **MVC pattern** to separate concerns between the model, view, and controller.

## Tools Used

- **Java Swing** for the graphical user interface (GUI)
- **C++** handles all game logic, including win conditions, player turns, and game state.
- **JNI** for communication between Java and C++ components.
- **JUnit 5** for unit testing the game logic and ensuring a smooth experience.

## Game Flow

1. **Game Setup**: 
   - The game starts by initializing a 5x5 grid for the Tic-Tac-Toe board.
   - Players take turns to mark a cell in the grid with either "X" or "O".

2. **Gameplay**:
   - The player or AI selects a cell to place their mark.
   - After each move, the game checks for a win condition (horizontal, vertical, diagonal).

3. **Win Condition**:
   - A player wins if they form a line of 5 marks horizontally, vertically, or diagonally.

4. **Graphics**:
   - The GUI updates dynamically after each move to reflect the state of the game.
   - Players are notified of wins or ties directly in the GUI.

## Running the Application

To run the **Checkers / Tic-Tac-Toe 5x5** game locally:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/CheckersTicTacToe5x5.git && cd CheckersTicTacToe5x5
2. Compile the C++ code:
  - Make sure to compile the C++ game logic before running the application. If you are using a typical setup, use the following command:
    ```bash
    g++ -shared -o libgameLogic.so game_logic.cpp
3. Run the Java application:
   - Build and run the project using Maven:
   ```bash
    mvn clean install
    mvn exec:java
   ```
4. Play the game:
  - Launch the game through the GUI, and start playing!

## Access the Game
  - The game interface is entirely graphical, offering click-able squares and updates for players to interact with the 5x5 board.

## Unit Testing
  Unit tests have been written to validate the core game logic, ensuring the correctness of game rules, win conditions, and turn-taking mechanisms. The tests are written using JUnit 5.
  - To run the tests:
  ```bash
  mvn test
  ```

## JNI Integration
  The Java code communicates with the C++ logic through JNI. This allows Java to leverage the performance of C++ while maintaining a user-friendly interface in Java.
