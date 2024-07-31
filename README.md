# SHA256Breaker

SHA256Breaker is a Python script that performs a brute-force attack on SHA-256 hashed passwords using a list of common passwords. It attempts to find the plaintext password that matches a given SHA-256 hash by comparing it against a list of common passwords.

### Features
- Attempts to crack SHA-256 hashes using a list of commonly used passwords.
- Provides real-time progress updates on the cracking attempt.
- Reports success or failure upon finding the matching password.

### Technologies Used
- Python 3
- `pwn` library for progress reporting and logging

### Usage
1. Clone the repository:
    ```bash
    git clone https://github.com/0xknoty/SHA256Breaker.git
    cd SHA256Breaker
    ```

2. Run the script:
    ```bash
    python SHA256Breaker.py <sha256sum>
    ```

3. Configuration:
    - Replace `<sha256sum>` with the SHA-256 hash you want to crack.
    - Ensure the `rockyou.txt` file is available at `/usr/share/wordlists/rockyou.txt` or update the `password_file` path in the script accordingly.

4. Execution:
    - The script will read passwords from the specified file and calculate their SHA-256 hashes.
    - It will compare each hash with the target hash and display progress and results in real-time.

### How It Works
- The script reads passwords from the specified wordlist file (`rockyou.txt`), encoding each password to bytes.
- For each password, it computes the SHA-256 hash.
- It compares the computed hash with the provided target SHA-256 hash.
- If a matching hash is found, it prints the successful password and stops further attempts.
- If no match is found after testing all passwords, it reports failure.

### Disclaimer!

**The author of this script is not responsible for any misuse or damages caused by using this script. Use it at your own risk.**
