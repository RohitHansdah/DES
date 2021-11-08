
# Implementing Data Encryption Algorithm


Write a program with a nice UI to implement and study DEA with different hyper
parameters.
Number of rounds n=1,8,16,32; half width of data block w=16,32,64. Pick suitable
entries for P- and S- boxes.
Demonstrate the avalanche effect with different hyper parameter choices.
Demonstrate how weak keys supplied by the user affects the round keys.
## Implementation details


The Data Encryption Standard (DES)
is a symmetric-key block cipher published by the
National Institute of Standards and Technology (NIST).
DES is an implementation of a Feistel Cipher. It uses 16 round Feistel structure.
The block size is 64-bit. Though, key length is 64-bit,
DES has an effective key length of 56 bits, since 8 of the
64 bits of the key are not used by the encryption algorithm
Since DES is based on the Feistel Cipher, all that is required to specify DES is:
Round function
Key schedule
Any additional processing − Initial and final permutation
Round function:
The heart of this cipher is the DES function, f.
The DES function applies a 48-bit key to the rightmost 32 bits to produce a 32-bit
output.
Initial and Final Permutation:
The initial and final permutations are straight Permutation boxes (P-boxes)
that are inverses of each other.
They have no cryptography significance in DES.
Expansion Permutation Box:
Since right input is 32-bit and round key is a 48-bit,
we first need to expand right input to 48 bits.
Key Generation:
The round-key generator creates sixteen 48-bit keys out of a 56-bit cipher key.
DES Analysis:
The DES satisfies both the desired properties of block cipher. These two properties
make cipher very strong.
Avalanche effect − A small change in plaintext results in the very great change in
the ciphertext.
Completeness − Each bit of ciphertext depends on many bits of plaintext.
During the last few years, cryptanalysis have found some weaknesses in DES when key
selected are weak keys.
These keys shall be avoided.
DES has proved to be a very well designed block cipher.
There have been no significant cryptanalytic attacks on DES other than exhaustive
key search.
## Screenshots

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRimLU66mKJ8R1UHJypkFbqb6rCIJizvik85Q&usqp=CAU)

![](https://user-images.githubusercontent.com/44118554/140682830-896086f4-0ce5-44b2-b2cd-8cf13706126a.PNG)

![](https://user-images.githubusercontent.com/44118554/140682975-b5e00ef2-1604-4407-bfb7-c47bc826dc63.PNG)

![](https://user-images.githubusercontent.com/44118554/140652814-a4a3d5b2-155a-4c26-9ae6-59635818ee3d.PNG)

![](https://user-images.githubusercontent.com/44118554/140652672-f7464f75-6fbb-41f9-b35c-8138fbf7dc51.PNG)

![](https://user-images.githubusercontent.com/44118554/140652725-794806e0-9411-4706-ae2c-d761c39c1eda.PNG)


## Run Locally

Clone the project

```bash
  git clone https://github.com/RohitHansdah/DES
```

Go to the project directory

```bash
  cd code.py
```

Install dependencies

```bash
  pip install tk
```




## Demo

![GIF](https://i.makeagif.com/media/11-08-2021/1PDBjk.gif)


## Documentation

[Report](https://drive.google.com/file/d/1Q9hHzj1NJsNhgF-DCb5eVFSC4w-CBHtY/view?usp=sharing)


## Conclusion

Advantages:
DES is broken; however, 3DES is currently considered a secure cipher.
DES does have the desirable properties of confusion and diffusion:
each bit of ciphertext is based upon multiple bits of the key and changing a single
bit of plaintext changes, on average, half of the bits of ciphertext.
Due to its Feistel structure and uncomplicated logic, DES is relatively easy to
implement.However, it uses eight distinct S-Boxes, which increases its footprint (AES uses a
single S-Box).

Disadvantages:
The main disadvantage to DES is that it is broken using brute-force search.
However, using 3DES mitigates this issue at the cost of increasing execution time.
DES is also vulnerable to attacks using linear cryptanalysis. However, it takes 247
known plaintexts to break DES in this manner.
