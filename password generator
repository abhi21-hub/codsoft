import random
import string

def generate_password(length, use_uppercase=True, use_lowercase=True, use_digits=True, use_special=True):
    character_set = ''
    
    if use_uppercase:
        character_set += string.ascii_uppercase
    if use_lowercase:
        character_set += string.ascii_lowercase
    if use_digits:
        character_set += string.digits
    if use_special:
        character_set += string.punctuation

    if not character_set:
        raise ValueError("At least one character type must be selected.")

    password = ''.join(random.choice(character_set) for _ in range(length))
    return password

def main():
    try:
        length = int(input("Enter the desired length of the password: "))
        if length <= 0:
            raise ValueError("Password length must be greater than zero.")

        use_uppercase = input("Include uppercase letters? (y/n): ").strip().lower() == 'y'
        use_lowercase = input("Include lowercase letters? (y/n): ").strip().lower() == 'y'
        use_digits = input("Include digits? (y/n): ").strip().lower() == 'y'
        use_special = input("Include special characters? (y/n): ").strip().lower() == 'y'

        password = generate_password(length, use_uppercase, use_lowercase, use_digits, use_special)
        print(f"Generated password: {password}")
    except ValueError as e:
        print(f"Error: {e}")

if _name_ == "_main_":
    main()
