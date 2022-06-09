class Solution {
    public void sortColors(int[] nums) {
        int low=0;
        int mid=0;
        int high=nums.length-1;
        while(mid<=high){
            if(nums[mid]==0){
                int temp=nums[mid];
                nums[mid]=nums[low];
                nums[low]=temp;
                mid++;
                low++;
            }
            else if(nums[mid]==1){
                mid++;
            }
            else if(nums[mid]==2){
                int temp=nums[mid];
                nums[mid]=nums[high];
                nums[high]=temp;
                high--;
            }
        }
        //BRUTE FORCE
//        int zero=0;
//         int one=0;
//         int two=0;
//         for(int i=0;i<nums.length;i++){
//             if(nums[i]==0)zero++;
//             if(nums[i]==1)one++;
//             if(nums[i]==2)two++;
//         }
//         int ans=0;
//         while(zero>0){
//         nums[ans++]=0;
//           zero--;
//          }
    
//         while(one>0){
//         nums[ans++]=1;
       
//         one--;
//     }
      
//         while(two>0){
//         nums[ans++]=2;
      
//         two--;
//         }
    }
}
