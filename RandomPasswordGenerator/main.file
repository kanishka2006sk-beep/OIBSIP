import random
import string

print("===== RANDOM PASSWORD GENERATOR =====")

while True:
    try:
        length = int(input("Enter password length (minimum 8): "))

        if length < 8:
            print("Password length must be at least 8 characters.")
            continue

        print("\nSelect character types:")
        print("1. Uppercase Letters")
        print("2. Lowercase Letters")
        print("3. Numbers")
        print("4. Symbols")

        characters = ""

        if input("Include Uppercase? (y/n): ").lower() == "y":
            characters += string.ascii_uppercase

        if input("Include Lowercase? (y/n): ").lower() == "y":
            characters += string.ascii_lowercase

        if input("Include Numbers? (y/n): ").lower() == "y":
            characters += string.digits

        if input("Include Symbols? (y/n): ").lower() == "y":
            characters += string.punctuation

        if characters == "":
            print("Please select at least one character type.")
            continue

        password = "".join(random.choice(characters) for _ in range(length))

        print("\nGenerated Password:", password)

        again = input("\nGenerate another password? (y/n): ").lower()

        if again != "y":
            print("Thank you!")
            break

    except ValueError:
        print("Please enter a valid number.")
