# microit-1
password generator
import random
import string

def generate_password(length=12, use_special_chars=True):
    # Base character set: letters and digits
    chars = string.ascii_letters + string.digits
    if use_special_chars:
        chars += string.punctuation

    # Ensure the length is valid
    if length < 4:
        raise ValueError("Password length should be at least 4 characters.")

    # Generate the password
    password = ''.join(random.choice(chars) for _ in range(length))
    return password

# Example usage
password = generate_password(length=16, use_special_chars=True)
print("Generated Password:", password)
