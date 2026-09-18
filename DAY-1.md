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


Question no. 15 Longest Consecutive Sequence

Solution :

class Solution {
public:
    int longestConsecutive(vector<int>& nums) {
       unordered_set<int> st(nums.begin(),nums.end());
       int answer =0;
       for(auto v:st){
        int count=0;
        int current = v;
        if(st.count(current-1)){
            continue;
        }
         else{
            current+=1;
            while(st.count(current)){
                count++;
                current++;
            }
         }

 answer =max(answer,count+1);
       }
       return answer;
    }
};
<img width="1440" height="900" alt="Screenshot 2026-09-18 at 11 05 39 AM" src="https://github.com/user-attachments/assets/5591dc42-64b6-4c4e-be8e-39f645553071" />


Question no.30 Valid Parentheses

Solution :

lass Solution {
public:
    bool isValid(string s) {
        stack<char>st;
        for(auto v:s){
            if(v=='(' || v=='{'||v=='['){
          st.push(v);
            }
            else{
              if (st.empty()){
                return false;
              }
              if((v == ')' && st.top() == '(') || (v == ']' && st.top() == '[')|| (v == '}' && st.top() == '{')){
                st.pop();
            }
            else{
                return false;
            }
        }
        }
    
return st.size()==0;
    }
};

<img width="1440" height="900" alt="Screenshot 2026-09-18 at 12 22 30 PM" src="https://github.com/user-attachments/assets/bcf084fd-2eab-426e-a001-7638234937cf" />

