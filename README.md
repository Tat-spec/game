# gameimport random

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    
    # The computer randomly selects a number between 1 and 100
    number_to_guess = random.randint(1, 100)
    
    attempts = 0
    guess = None
    
    # Loop until the player guesses the correct number
    while guess != number_to_guess:
        try:
            # Get player's guess
            guess = int(input("Enter your guess (between 1 and 100): "))
            attempts += 1
            
            # Check if the guess is too high, too low, or correct
            if guess < number_to_guess:
                print("Too low! Try again.")
            elif guess > number_to_guess:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You guessed the number {number_to_guess} in {attempts} attempts.")
        except ValueError:
            print("Invalid input! Please enter a valid number.")

# Run the game
number_guessing_game()
