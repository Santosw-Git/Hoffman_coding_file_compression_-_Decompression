# Huffman Coding File Compression and Decompression

## Description
This is the project which I did in my 4th semester as part of the **Data Structures and Algorithms** subject. In this project, I implemented the **Huffman Coding Algorithm** for file compression and decompression. The algorithm is used to compress text files by encoding characters into variable-length codes based on their frequencies in the file. The project includes functionalities for both compressing and decompressing text files.

### Features:
- **File Compression**: Compresses a text file using Huffman coding.
- **File Decompression**: Decompresses the `.bin` file and restores the original text.
- **Efficient Data Encoding**: Uses shorter codes for frequent characters and longer codes for less frequent ones.
- **Padding**: Adds necessary padding to ensure that the final binary string is a multiple of 8 bits for storage.
  
## How it Works
1. **Compression**:
    - The program reads the input text file and calculates the frequency of each character.
    - A **Huffman Tree** is built using the character frequencies, where the most frequent characters are assigned shorter codes.
    - The text is encoded into a binary string using these codes.
    - Padding is added to ensure that the binary string is a multiple of 8 bits.
    - The binary string is then converted into bytes and saved in a `.bin` file.

2. **Decompression**:
    - The program reads the compressed `.bin` file, extracts the binary data, and removes the padding.
    - The binary data is decoded using the Huffman Tree to reconstruct the original text.

## Requirements
- C++ Compiler (C++11 or later)
- Standard C++ libraries (`<bits/stdc++.h>`, `<fstream>`, `<bitset>`)

## How to Use
1. **Compile the Program**:
    - Use a C++ compiler to compile the project:
      ```bash
      g++ -o huffman_compression_decompression huffman_compression_decompression.cpp
      ```

2. **Run the Program**:
    - Create an object of the `HuffmanCode` class by providing the path to the input text file:
      ```cpp
      HuffmanCode huff("./input.txt");  // path to the input file
      huff.compressFile();              // Compress the file
      huff.decompressFile();            // Decompress the file
      ```

3. **Input and Output**:
    - The program generates a `.bin` compressed file and a `.txt` decompressed file.

### Sample Input:
