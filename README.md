# python2
random password generator
import random
import string

def generate_password(length):
    if length < 4:
        return "Password should be at least 4 characters long."

    # Create pools of characters
    all_chars = string.ascii_letters + string.digits + string.punctuation

    # Randomly choose characters
    password = ''.join(random.choice(all_chars) for _ in range(length))
    return password

try:
    user_length = int(input("Enter password length: "))
    password = generate_password(user_length)
    print(f"\nGenerated password: {password}")

except ValueError:
    print("❌ Please enter a valid number.")
