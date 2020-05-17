# LeetCode #Recursion
class Solution {
   
   
   public int maxDepth(TreeNode root) {
        if(root==null) 
        {
            return 0; 
        }
        
        else {
        int leftHeight=getHeight(root.left,1);
        int rightHeight=getHeight(root.right,1);
        
        return Math.max(leftHeight,rightHeight);
    
    }
    }
    private int getHeight(TreeNode n, int height){
        if(n==null) return height;
        
        return Math.max((getHeight(n.left,height+1)), getHeight(n.right,height+1));
    }
}
