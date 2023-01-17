import random
import string

def generate_password(length):
    # Create a list of characters to include in the password
    characters = string.ascii_letters + string.digits + string.punctuation

    # Use the random.choices() function to generate a list of random characters of the desired length
    password = "".join(random.choices(characters, k=length))

    return password

# Prompt the user for the desired password length
length = int(input("Enter the desired length of the password: "))

# Generate and print the password
password = generate_password(length)
print("Generated password:", password)
