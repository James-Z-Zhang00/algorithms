# algorithms

Here I share my own study about algorithms as a part of my developer journey, hope it can be helpful to other people too.

<details>
  <summary>RSA (Rivest-Shamir-Adleman) Asymmetric Cryptographic Algorithm</summary>
  
  1. Key Generation:
    * Choose 2 distinct prime numbers _`p`_ and _`q`_
    * Computer their product, _`n = p X q`_ which becomes the modulus for both the public and private keys
    * Compute the totient of _`n`_ denoted as *φ(n)* where _`φ(n) = (p - 1) * (q - 1)`_
    * Choose an integer _`e`_ such that _`1 < e < φ(n)`_ and _`e`_ is coprime with _`φ(n)`_ where _`e`_ is the public exponent
    * Compute the modular multiplicative inverse of _`e`_ modulo _`φ(n)`_, denoted as _`d`_, where _`d * e ≡ 1 (mod φ(n))`_ where d is the private exponent
    * The public key consists of _`(n, e)`_, and the private key consists of _`(n, d)`_
2. Encryption:
    * To encrypt a message _`M`_, the sender uses the recipient`s public key _`(n, e)`_
    * Convert the message _`M`_ into an integer m such that _`0 ≤ m < n`_
    * Compute the ciphertext _`C`_ using the formula _`C ≡ m^e (mod n)`_
    * Send the ciphertext _`C`_ to the recipient
3. Decryption:
    * To decrypt the ciphertext _`C`_, the recipient uses their private key _`(n, d)`_
    * Compute the plaintext _`M`_ using the formula _`M ≡ C^d (mod n)`_
    * Convert the integer _`M`_ back into the original message
</details>

