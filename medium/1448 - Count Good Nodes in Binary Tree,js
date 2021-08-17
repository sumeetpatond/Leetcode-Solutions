/**
 * Definition for a binary tree node.
 * class TreeNode {
 *     val: number
 *     left: TreeNode | null
 *     right: TreeNode | null
 *     constructor(val?: number, left?: TreeNode | null, right?: TreeNode | null) {
 *         this.val = (val===undefined ? 0 : val)
 *         this.left = (left===undefined ? null : left)
 *         this.right = (right===undefined ? null : right)
 *     }
 * }
 */

function goodNodes(root: TreeNode | null): number {
    
    const dfs = function(node: TreeNode | null, currentMax: number){
        const newCurrentMax = Math.max(currentMax, node.val);
        
        const lhsCount = node.left == null ? 0 : dfs(node.left, newCurrentMax)
        
        const currentCount = node.val >= currentMax? 1: 0;
        
        const rhsCount = node.right == null ? 0 : dfs(node.right, newCurrentMax)

        return lhsCount + currentCount + rhsCount;
    }
    
    if(root==null) return 0;
    return dfs(root, root.val)
};
