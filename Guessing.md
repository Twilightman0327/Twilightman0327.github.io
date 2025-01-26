## Flowchart  
```mermaid
flowchart TD
    Start([Start]) --> Init[Initialize game]
    Init --> RNG[Generate random number within range]
    RNG --> Prompt[Prompt user for a guess]
    Prompt --> Validate[Validate user input]
    Validate -->|Invalid input| Error[Display error message and re-prompt user]
    Error --> Prompt
    Validate -->|Valid input| Compare[Check if guess matches random number]
    Compare -->|Too High| High[Inform user guess is too high]
    Compare -->|Too Low| Low[Inform user guess is too low]
    Compare -->|Correct| Correct[Congratulate user]
    High --> Prompt
    Low --> Prompt
    Correct --> End([End])

Start: The game begins. Initialation steps are prepared.
Initialize game: A random number is generated in a specific range.
Prompt user for a guess: user is prompted to input their guess.
Validate user input: If the input is invaled, error message is displayed and prompt user again.
Compare the guesses: If the guess is to high, prompt the user to guess again.  If the guess is to low, prompt the user to guess again. If the guess is correct, congratulate and end the game.
End: game is over after the user guesses the correct number.
