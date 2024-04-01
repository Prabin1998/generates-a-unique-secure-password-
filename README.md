import random
import string

def generate_password(length=12):
    # Define character sets for the password
    lowercase_letters = string.ascii_lowercase
    uppercase_letters = string.ascii_uppercase
    digits = string.digits
    special_characters = "!@#$%^&*()_+[]{}|;:,.<>?~"

    # Combine all character sets
    all_characters = lowercase_letters + uppercase_letters + digits + special_characters

    # Generate a random password
    password = "".join(random.choice(all_characters) for _ in range(length))
    return password

if __name__ == "__main__":
    password_length = 16  # You can adjust the desired length
    secure_password = generate_password(password_length)
    print(f"Your secure password: {secure_password}")
    
