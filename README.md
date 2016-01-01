# LeetCodeOJ1
LeetCodeOJ Question 1

Question 1:


Given an array of integers, find two numbers such that they add up to a specific tartget number.

The function towSum should return indices of the two numbers such that they add up to the target, where index1 must be less than index2. Please note that your returned answers(both index1 and index2) are not zero-based.

You may assume that each input would have exactly one solution.

**Input:** numbers = {2, 7, 11, 15}, target=9 
**output:** index1 = 1, index2 = 2

Solution 1:

	public class Solution {
    	public int[] twoSum(int[] nums, int target) {
        	int[] result = new int[2];
        	for(int i=0; i<nums.length;i++){
            	for(int j=i+1; j<nums.length; j++){
                	if(nums[i]+nums[j]==target){
                   	 result[0] = i+1;
                   	 result[1] = j+1;
                   	 return result;
                	}
            	}
        	}
        	return result;
    	}
	}