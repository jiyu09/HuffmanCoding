# Huffman Code Description

## HuffmanNode Class
This class includes the __init__ function that defines the frequency and name (symbol) of each node, and the left and right child nodes.
In other words, this class creates an object that includes information about each node.

## HuffmanCoding Class
This class creates a tree structure by sorting each node based on its frequency and writes a Huffman code.
### __init__ Function
This function creates a list of objects (defined as nodes in the class) for each node with the given data.
The data is received in the form of a dictionary with the symbols of the nodes that will become leaf nodes as keys and the frequencies as values.

### is_leaf Function
This function receives a node as an argument and determines whether the given node is a leaf node based on whether or not the object has a child node.

### get_codes function
Sort the list containing each object based on the frequency of each object, and define the two nodes at the front (the two objects with the lowest frequency) as left and right nodes, respectively.
Exclude the left and right nodes from the list containing the object, and add a new node with the frequency of the left and right nodes added.
=> Repeat until the length of the list containing the object becomes 1, and obtain a tree structure sorted based on the frequency.

After defining the root node, generate codes from the root node to each leaf node.
Return the generated final code.

### _get_codes function
This function writes the final code when the tree structure sorted by frequency is completed.
Receives a node, adds 0 to the left node of that node, and repeats this to generate the final Huffman code.
If the received node is a leaf node, return the final Huffman code as codes.
