flowchart TD
 Start([Start]) --> Init[0 to 175]
 Init --> Generate[Random number inbetween min and max numbers]
 Generate --> Guess[Guess a number]
 Guess --> ReviewInput{Has to be a number}

 ReviewInput -- No --> Error[Display 'Please use a valid number and try again.'] --> Guess
 ReviewInput -- Yes --> ReviewRange{has to guess within range}

 ReviewRange -- Yes --> Check{Was the correct number guessed?}
 ReviewRange -- No --> NotInRange[Display 'Not within range, guess again.']

 Check -- No --> HighOrLow{was the guess higher?}
 
 HighOrLow -- No --> TooLow[Display 'Too high.'] --> Guess
 HighOrLow -- Yes --> TooHigh[Display 'Too low.'] --> Guess
 
 Check -- Yes --> Correct[Display 'You guessed it right!']
 Correct --> End([End])

# **Code Descriptions**  
_**Start**_ : _Game Starts._       
_**Init**_ : _The minimun and maximun number range._    
_**Generate**_ : _A random number is selected by program._   
_**Guess**_ : _The number the player guessed._   
_**ReviewInput**_: _Checks to make sure they pick a number._   
_**ReviewRange**_: _Checks to make sure the number is within the set min and max numbers._  
_**Check**_: _Checks if the answer is correct. If not it gives a hint. If correct the game ends._  
_**Hint**_: _Tells you if you need to go lower or higher._  
_**Correct**_: _Correct guess._




