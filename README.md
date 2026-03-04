# tippitytappity-design

tippitytappity is a program to practice typing

## Data model

```mermaid
classDiagram
  class TypingTester{
        - runTest(): Score
  }
  class AccuracyTester{
        - userText: string
        - correctAnswer: string
        - setCorrectAnswer(string)
        + generateNewString(): void
        + checkAccuracy(string): double
  }
  class SpeedTester{
        - wpm: double
        - keystrokes: int
        - timeElapsed: TIME
        + getTypingSpeed(): int
  }
  class Score{
        THIS IS A STRUCT
        WPM: int
        Accuracy: double
  }
  class User{
        + Name: string
        - Password: string
        - email: string
        - scoreHistory: vector ~Score~
        + addNewScore(Score): void
  }
TypingTester <-- AccuracyTester
TypingTester <-- SpeedTester
User <-- Score
Score <-- TypingTester
```
