Question 1 Move Zeroes

Solution:
class Solution {
public:
    void moveZeroes(vector<int>& nums) {
        int j = 0;   
for (int i = 0; i < nums.size(); i++) {
            if (nums[i] != 0) {
                swap(nums[i], nums[j]);
                j++;
            }
        }
    }
};

<img width="1440" height="900" alt="Screenshot 2026-09-18 at 10 53 14 AM" src="https://github.com/user-attachments/assets/2c6983b9-0f7f-49f9-b9af-8c1d093be23b" />


Question 2 Majority Elements

Solution:

class Solution {
public:
    int majorityElement(vector<int>& nums) {
        int n=nums.size();
       
 sort (nums.begin(), nums.end());
   return nums[n/2];
   }
   };
     <img width="1440" height="900" alt="Screenshot 2026-09-18 at 11 01 26 AM" src="https://github.com/user-attachments/assets/e6ee8614-1346-4cf3-9575-b9f4f5a8015d" />
