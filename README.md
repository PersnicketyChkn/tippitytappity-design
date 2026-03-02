# tippitytappity-design

tippitytappity is a program to practice typing

## Data model

```mermaid
classDiagram
  class InputHandler{
        - userText: string
        - readInput(): string
  }
  class AccuracyTester{
        - userText: string
        - correctAnswer: string
        + checkAccuracy(string): string
        - setCorrectAnswer(string)
  }
  class SpeedTester{
        - wpm: double
        - keystrokes: int
        - timeElapsed: TIME
        + getTypingSpeed()
  }
  class User{
        + Name: string
        - Password: string
        - email: string
        - highscore: int
        + updateHighscore(int): void
  }
  class Scoreboard{
        + LeaderboardUsers: vector~User~
        + clearScoreboard(): void
        + addToScoreboard(User): void
        + displayScoreboard(): void
  }
```
