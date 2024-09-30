# Mermaid-GitHub
flowchart TD
    Start([Start]) --> GenerateRandomNumber["Generate Random Number"]
    GenerateRandomNumber --> UserInput["Get User Guess"]
    UserInput --> CheckValidInput{"Is Input Valid?"}
    CheckValidInput -- Yes --> CheckGuess{"Is Guess Correct?"}
    CheckValidInput -- No --> InvalidInput["Display 'Invalid Input' Message"] --> UserInput
    CheckGuess -- Too High --> TooHigh["Display 'Too High'"] --> UserInput
    CheckGuess -- Too Low --> TooLow["Display 'Too Low'"] --> UserInput
    CheckGuess -- Correct --> CorrectGuess["Display 'Correct Guess' Message"] --> End([End])
