# Daily-Leetcode-problem-solution11
PROBLEM

PROBLEM

We run a preorder depth-first search (DFS) on the root of a binary tree. At each node in this traversal, we output D dashes (where D is the depth of this node), then we output the value of this node. If the depth of a node is D, the depth of its immediate child is D + 1. The depth of the root node is 0. If a node has only one child, that child is guaranteed to be the left child. Given the output traversal of this traversal, recover the tree and return its root.

Intuition

Reconstruct the binary tree from the preorder DFS traversal string

Approach

1. Parse the traversal string: Identify the depth (counting dashes) and node values.
2. Use a stack: Maintain a stack to keep track of nodes at different depths.
   
3. Attach nodes correctly:
   
If the current node has a depth greater than the top node in the stack, it is the left child. If the current node has a depth equal to or less than the top node, pop the stack to find the correct parent. 
4. Attach the new node as either a left or right child accordingly. 
5. We iterate through the traversal string while tracking depths and values. A stack maintains the path from the root to the current node. 

6. At each step:

7. We adjust the stack to ensure it contains only nodes relevant to the current depth. If necessary, we attach the node to the appropriate parent. 7. The root node remains at the bottom of the stack at the end.

Complexity

Time complexity:

O(N), where N is the length of the traversal string (since we traverse the string once).

Space complexity:

O(H), where H is the height of the tree (for storing nodes in the stack).
