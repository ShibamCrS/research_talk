# AES History
Now we will discuss about the cipher Advanced Encryption Standard (AES).
This is currently the most wide used block cipher in the world.
Before going into the mathematics behind AES, we will go into the history of AES. This history is also important to understand how standarization works.

In 1997 NIST announced a competition to design a block cipher. It is public competition and anyone can submit a cipher. Then it was open for the public analysis. It is important to know that unlike public key cryptography, where the security depends on some hard mathmatical problem like factorization or lattice, the security of symmetric ciphers depends on public analysis.

Anyway, in 1999, out of 15 submission, 5 finalists were selected.
Later in 2000, AES was selected as the winner and NIST announced it as the standard.

# Design of AES
This is an SP Network, we will see soon what it means.
The block size if 128 bits, i.e., each element is binary 128 bit or a vecor of size 128 over GF(2) or vector of size 16 over GF(256). We interchange between these algebraic structures as needed.
The key size is 128, 192 or 256, depending on the secuirty level.

As I said, it is an iterated cipher. Each round function looks like this.
There are 4 operations in each round:

1. SubBytes
2. Shift rows
3. Mix columns
4. Add round key

Among these only SubByte is a non linear function, the others are linear. This SubBytes is actually substitution and linear part is permutation. Together it is a substitution permutation network.

Though ARK is linear, I have kept it as a sperate function to make the notation clear. As we discussed in the introduction that the round function is itself key independent.

# The mix column function

Mixcolumn operates on each columns parallelly (see in the board). To define this multiplication, we need fix the algebraic representation. We will talk about Galois Field with 2^8 elements:

