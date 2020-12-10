# HuffmanCoding

##Summary

Huffman coding is an algorithm that achieve lossless encoding. The procedure behind its scheme includes categorizing numerical values from a set-in order of their frequency. The minimal frequency numbers are gradually eliminated via the Huffman tree, that adds minimal frequency from the sorted list in every new branch. The sum is then positioned above the two eliminated minimal frequency values and replace them in the new sorted list. For every new branch, the algorithm moves the direction of the tree either right or to the left where right ones are higher values and left ones are lower values. When sorted list is done then the tree is complete, the final value is zero if the tree ended on a left number, or it is one if it ended on the right.

##Huffman Algorithms

Huffman coding comprises of 2 algorithm techniques to successfully encode and decode files.  

###Compression Algorithm

•	Build frequency dictionary.
•	Build priority queue.
•	Build Huffman tree by selecting 2 min nodes and merging them.
•	Assign codes to characters.
•	Encode the input text.
•	If overall length of bit stream is not multiple of 8, add some padding to the text.
•	Store the padding information (in 8 bits) at the start of the overall encoded bit stream.
•	Write the result to an output binary file.

###Decompression Algorithm

•	Read binary file.
•	Read padding information. Removed the padded bits.
•	Decode the bits, read the bits and replace the valid Huffman code bits with the character values.
•	Save the decoded data into output file.

##Testing




