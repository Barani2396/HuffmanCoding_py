# HuffmanCoding

## Summary

Huffman coding is an algorithm that achieve lossless encoding. The procedure behind its scheme includes categorizing numerical values from a set-in order of their frequency. The minimal frequency numbers are gradually eliminated via the Huffman tree, that adds minimal frequency from the sorted list in every new branch. The sum is then positioned above the two eliminated minimal frequency values and replace them in the new sorted list. For every new branch, the algorithm moves the direction of the tree either right or to the left where right ones are higher values and left ones are lower values. When sorted list is done then the tree is complete, the final value is zero if the tree ended on a left number, or it is one if it ended on the right.

## Huffman Algorithm

Huffman coding comprises of 2 algorithm techniques to successfully encode and decode files. The below set of rules are implemented in the source file.

### Compression Algorithm

-	Build frequency dictionary.
-	Build priority queue.
-	Build Huffman tree by selecting 2 min nodes and merging them.
-	Assign codes to characters.
-	Encode the input text.
-	If overall length of bit stream is not multiple of 8, add some padding to the text.
-	Store the padding information (in 8 bits) at the start of the overall encoded bit stream.
-	Write the result to an output binary file.

### Decompression Algorithm

-	Read binary file.
-	Read padding information. Removed the padded bits.
-	Decode the bits, read the bits and replace the valid Huffman code bits with the character values.
-	Save the decoded data into output file.

## Testing

Follow the below instructions to try out the huffman coding,

### Compression

-	Save the above code in a folder with `.py` extension, ex: `hc.py`
-	Run terminal and navigate to the `hc.py` folder
-	Start python3 shell by entering `python3`
-	Then import the class “HuffmanCoding” from the `hc.py` file by inputting `from hc import HuffmanCoding`
-	Create a `sample.txt` file, with some texts, in the same folder
-	Initialize the `path` variable to the `sample.txt` file location, ex: `path=/Users/*****/sample.txt`
-	Instantiate an object to use the `compressor` method, `H = HuffmanCoding(path)`
-	Call the `compressor()` method to create a compressed binary file, ex: `H.compressor()`

### Decompression

Calling the `decompressor()` method would get back the content of `sample.txt` file, ex: `H.decopress('/Users/**** /sample.bin')`

## Results

Size comparisson before and after the huffman code applied.

### Sample File
<img src="/imgs/samp.jpg" height="325" width="325">

### Compressed File
<img src="/imgs/comp.jpg" height="300" width="300">

### Decompressed File
<img src="/imgs/decomp.jpg" height="300" width="300">

| Sample File  | Compressed File | Decompressed File |
| ------------- | ------------- | ------------- |
| Content Cell  | Content Cell  | <img src="/imgs/decomp.jpg" height="350" width="350"> |















