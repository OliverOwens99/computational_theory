# Computational Theory

---

## Task 1 : Binary Representations

Implemented core bitwise operations used in cryptographic algorithms:

rotl - Circular rotation of bits to the left
rotr - Circular rotation of bits to the right
ch - Choose function that selects bits from y or z based on bits in x
maj - Majority function that performs bit-wise voting
Key optimizations include using masking with 0xFFFFFFFF to ensure proper 32-bit boundaries and implementing XOR patterns for efficient bit selection.

---
## Task 2: Hash Functions

Implemented a basic hash function based on the algorithm from Kernighan & Ritchie's "The C Programming Language":

- Uses multiplication by 31 (prime near power of 2) for good bit distribution
- Applies modulo 101 (prime near 100) to create a bounded output range
- Processes input character-by-character, building a scrambled hash value
The implementation demonstrates how simple mathematical operations can create effective one-way transformations for data indexing. The reason why these two integers work is a mystery.
---
## Task 3: SHA256

Created a function to calculate SHA-256 padding for arbitrary file inputs:

- Adds a single '1' bit (represented as 0x80 byte) after the message
- Appends '0' bits until message length is 64 bits short of multiple of 512
- Finishes with the 64-bit representation of the original message length
This illustrates a key component of the SHA-256 cryptographic hash function used in modern security applications.
---
## Task 4: Prime Numbers

Implemented and compared two fundamental prime number generation algorithms:

- Sieve of Eratosthenes - Ancient algorithm with O(n log log n) time complexity
- Trial Division - Basic approach with optimizations to check only numbers of form 6k±1
Analysis includes time/space complexity comparisons and discussions of optimisation techniques like starting inner loops at i² instead of 2i.
---
## Task 5: Roots
Explored binary representations of square roots of prime numbers:

- Generated the first 32 bits of the fractional parts of square roots
- Created a tabular display showing binary and hexadecimal representations
- Discussed applications in cryptography as "nothing-up-my-sleeve numbers"
This task demonstrates how irrational numbers provide high-quality pseudo-random bit sequences.
---
## Task 6: Proof of Work
Searched for English words with the most leading zero bits in their SHA-256 hash:

- Processed a dictionary of English words, computing SHA-256 hashes
- Implemented an efficient two-phase zero-counting algorithm
- Found "APPLICANT" had the most leading zeros (16)
This connects directly to blockchain mining concepts where finding values with many leading zeros is the central challenge.
---
## Task 7: Turing Machines
Implemented a binary increment Turing machine:

- Created a 3-state machine (Scan, Carry, Halt) that adds 1 to binary numbers
- Defined a state transition table modeling the carry operation in binary addition
- Successfully tested with multiple examples including overflow cases (e.g., 1111 → 10000)

This demonstrates one of the fundamental examples of a Turing machine performing a practical computation while handling all edge cases, including carrying operations and number expansion.
---
## Task 8: Computational Complexity

Analysed the computational complexity of sorting algorithms with focus on bubble sort:

- Implemented bubble sort with early termination optimisation
- Tested all permutations of [1,2,3,4,5] to demonstrate performance characteristics
- Compared with better algorithms like merge sort (O(n log n)) and quick sort
- Discussed factors that influence algorithm selection in practice
The analysis shows how small optimizations can significantly improve performance in specific cases.
---
## References

1. National Institute of Standards and Technology (2015). FIPS PUB 180-4: Secure Hash Standard (SHS). Section 2.2.2: Elementary Functions.https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.180-4.pdf  
2. The C programming Lanaguage by DENNIS M.RITCHIE and BRIAN W. KERNIGHAN
https://seriouscomputerist.atariverse.com/media/pdf/book/C%20Programming%20Language%20-%202nd%20Edition%20(OCR).pdf  
3. Turing, A. M. (1936). "On Computable Numbers, with an Application to the Entscheidungsproblem." Proceedings of the London Mathematical Society, Series 2, Volume 42, Issue 1, pp. 230-265.https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf
4. Bubble sort explaination,w3schools. https://www.w3schools.com/dsa/dsa_algo_bubblesort.php#:~:text=The%20Bubble%20Sort%20algorithm%20loops,again%20and%20again%20n%20times.
5. Sieve of Eratosthenes code: https://www.geeksforgeeks.org/python-program-for-sieve-of-eratosthenes/
6. Trail Divison :https://www.geeksforgeeks.org/trial-division-algorithm-for-prime-factorization/
7. Root cubes help :https://github.com/ianmcloughlin/computational_theory/blob/main/materials/cube_roots.ipynb
