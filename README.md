# Algo-Tree-Search
This is created to save knowledge about Tree Search Problem

## Most obvious use case
For the problem we need to search the BST or any kind of tree 

## DFS
The most common problem:
- [Range Sum of BST](https://leetcode.com/problems/range-sum-of-bst/?envType=daily-question&envId=2024-01-08) [Solution✔️]
- [Leaf-Similar Trees](https://leetcode.com/problems/leaf-similar-trees/description/?envType=daily-question&envId=2024-01-08) [Solution✔️]

``` Python 3
def rangeSumBST(self, root: Optional[TreeNode], low: int, high: int) -> int:
        def dfs(curr:TreeNode, low, high):
            res = 0
            if curr == None:
                return 0
            if (curr.val >= low) & (curr.val <= high):
                res = curr.val
            sum_left = dfs(curr.left,low,high)
            sum_right = dfs(curr.right, low, high)

            return res + sum_left + sum_right
        return dfs(root, low, high)

```


## BFS
