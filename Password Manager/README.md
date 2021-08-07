# Password Manager

Organize and store your passowrds along with username or account name in a textfile but not storing the passwod in plain text - ecnrypting the password is done.

### About Fernet Module & Cryptography Package:
Python supports a cryptography package that helps us encrypt and decrypt data. 

The fernet module of the cryptography package has inbuilt functions for the generation of the key, encryption of plaintext into ciphertext, and decryption of ciphertext into plaintext using the encrypt and decrypt methods respectively.

`pip install cryptography`

The fernet module guarantees that data encrypted using it cannot be further manipulated or read without the key.

### Methods used from the Ferent Module:

`generate_key()` : This method generates a new fernet key. The key must be kept safe as it is the most important component to decrypt the ciphertext. If the key is lost then the user can no longer decrypt the message. Also if an intruder or hacker gets access to the key they can not only read the data but also forge the data.

Note: You need to keep this key in a safe place. If you lose the key, you won't be able to decrypt the data that was encrypted with this key.

`encrypt(data)` : It encrypts data passed as a parameter to the method. The outcome of this encryption is known as a “Fernet token” which is basically the ciphertext. The encrypted token also contains the current timestamp when it was generated in plaintext. The encrypt method throws an exception if the data is not in bytes.

`decrypt(token)` : This method decrypts the Fernet token passed as a parameter to the method. On successful decryption the original plaintext is obtained as a result, otherwise an exception is thrown.


(Source: GeeksforGeeks)
