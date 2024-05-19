# AVL Tree Implementation

This code implements an AVL tree, which is a self-balancing binary search tree. Below is a brief description of the main components and functionalities of the code.

## Class AVLNode
- Represents a node in the tree containing a key, the height of the node, and references to the left and right subtrees.
- Method `__str__` provides a string representation of the tree.

## Helper Functions
- `get_height(node)`: Returns the height of the node or 0 if the node is None.
- `get_balance(node)`: Computes the balance factor of the node as the difference in heights of the left and right subtrees.
- `left_rotate(z)` and `right_rotate(y)`: Perform left and right rotations, respectively, to balance the tree.

## Tree Operations
- `tree_minimum(node)`: Finds the minimum value in the tree.
- `tree_maximum(node)`: Finds the maximum value in the tree.
- `tree_suma(node)`: Computes the sum of all keys in the tree.

## Node Insertion and Deletion
- `insert(root, key)`: Inserts a new node into the tree and performs necessary rotations to maintain balance.
- `delete_node(root, key)`: Deletes a node from the tree and performs necessary rotations to maintain balance.

## Main Block
- Creates an empty tree and inserts values from the list `keys`.
- Outputs the minimum value, maximum value, and the sum of all values in the tree.

## Usage
To use the AVL tree, simply run the script. The tree will be built using the values in the `keys` list, and it will output the minimum value, maximum value, and the sum of all values in the tree.

```python
if __name__ == "__main__":
    root = None
    keys = [5, 18, 33, 77, 2, 150, -2, 99]

    for key in keys:
        root = insert(root, key)
    print("Values used to build the tree:", keys)
    print("Minimum value in the AVL tree:", tree_minimum(root))
    print("Maximum value in the AVL tree:", tree_maximum(root))
    print("Sum of all values in the AVL tree:", tree_suma(root))
