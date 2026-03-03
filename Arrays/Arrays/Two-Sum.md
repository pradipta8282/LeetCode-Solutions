Brute force (using two pointer)


public class Solution {
    public int[] TwoSum(int[] nums, int target) {
       for(int i=0;i<nums.Length;i++){
        for(int j=i+1;j<nums.Length;j++){
            if(nums[i]+nums[j]==target){
                return new int[]{i,j};
            }
        }
       }
       return new int[] {0};

    }
};

Time Complexity:

O(n²)

 Space Complexity:

O(1)

optimized using Dictionary
public class Solution {
    public int[] TwoSum(int[] nums, int target) {
       Dictionary<int , int> map = new Dictionary<int,int>();
       for(int i=0;i<nums.Length;i++){
        int complement= target - nums[i];
        if(map.ContainsKey(complement)){
            return new int[]{map[complement],i};

 }
       else{
        map[nums[i]]=i;
       }
       }
       return new int[0];
    
 }
    
};

so here using dictionary..Dictionary time and space is we must inspect each element at least once, so O(n) is the lower bound. The HashMap approach achieves this optimal time complexity.
O(n)
O(n)
    
    
