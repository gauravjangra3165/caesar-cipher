# caesar-cipher
A lightweight Python utility for encrypting and decrypting messages with the Caesar cipher using a custom shift key.
# caesar-cipher
A lightweight Python utility for encrypting and decrypting messages with the Caesar cipher using a custom shift key.
CAESAR CIPHER PROJECT
=====================

A simple command-line program in Python that encrypts and decrypts text
using the Caesar cipher, a classic substitution technique where each
letter is shifted by a fixed number of positions in the alphabet.


FEATURES
--------
- Encrypt and decrypt text with a key between 1 and 25
- Preserves uppercase and lowercase letters
- Leaves spaces, digits, and punctuation unchanged
- Input validation for the key (rejects non-numbers and out-of-range values)
- Menu-driven interface that loops until you choose to quit


REQUIREMENTS
------------
- Python 3.6 or higher (uses f-strings)
- No external libraries needed


HOW TO RUN
----------
    python caesar_cipher.py

(Replace caesar_cipher.py with your actual file name.)


USAGE
-----
When the program starts, choose an option:

    e  -  Encrypt
    d  -  Decrypt
    q  -  Quit

Then enter a key (1-25) and the text to process.


EXAMPLE SESSION
---------------
    *****     CAESAR CIPHER PROGRAM     *****

    SELECT OPTION:
      e - ENCRYPT
      d - DECRYPT
      q - QUIT

    e/d/q: e

    ENCRYPTION MODE

    ENTER KEY (1-25): 3
    ENTER TEXT: Hello, World!

    RESULT: Khoor, Zruog!


HOW IT WORKS
------------
Each letter is converted to its position in the alphabet (a = 0, b = 1, ...),
shifted by the key using modular arithmetic (index + key) % 26, and converted
back to a letter. Decryption applies the same shift in the opposite direction
(-key). Non-alphabetic characters are passed through as they are.


PROJECT STRUCTURE
-----------------
    caesar_cipher.py   - Main program
    README.txt         - Project documentation


FUNCTIONS
---------
- shift_letter(letter, key)      : shifts a single letter and preserves its case
- Encrypt(plaintext, key)        : encrypts a full string
- Decrypt(ciphertext, key)       : decrypts a full string
- get_key()                      : prompts for and validates the key
- main()                         : runs the menu loop


POSSIBLE IMPROVEMENTS
---------------------
- Brute-force mode that tries all 25 keys
- Reading from and writing to files
- A GUI using Tkinter
