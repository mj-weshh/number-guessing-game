# Number Guessing Game

This Python script implements a simple number guessing game. The computer generates a random number between 1 and a specified maximum value, and the user tries to guess the correct number.

## How to Use
1. Clone the repository or download the `guessthenumbercomp.py` file.
2. Make sure you have Python installed on your system.
3. Run the script using a Python interpreter.

   ```bash
   python guessthenumbercomp.py
   ```

4. Follow the prompts to input your guess.
5. The script will provide feedback on whether your guess is too low, too high, or correct.

## Functionality

The script contains a function `guess(x)` that takes a maximum value `x` as an argument. The computer generates a random number between 1 and `x`, and the user is prompted to guess the number. The game provides feedback on each guess until the correct number is guessed.

```python
import random

def guess(x):
    random_number = random.randint(1, x)
    user_guess = 0

    while user_guess != random_number:
        user_guess = int(input(f'Guess a number between 1 and {x}: '))

        if user_guess < random_number:
            print("Sorry, guess is low!")
        elif user_guess > random_number:
            print("Sorry, guess is high!")

    print(f"Congratulations!! Your guess was right. The number was {random_number}")

# Example usage
guess(17)
```

## Input Example
```
Guess a number between 1 and 17: 8
```

## Output Example
```
Sorry, guess is low!
Guess a number between 1 and 17: 12
Sorry, guess is high!
Guess a number between 1 and 17: 10
Congratulations!! Your guess was right. The number was 10
```

Feel free to modify and use this script as needed!
