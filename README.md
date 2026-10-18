# DSA-Practice
My Leetcode solutions C++ 



class Solution{
public:
    vector<int> twoSum(vector<int>&num, int target){
        unordered_map<int,int> seen;
        int i;
       for(i=0;i<num.size();i++){
           int complement=target-num[i];
           if (seen.find(complement)!=seen.end()){
             return{seen[complement],i};
                 }
            seen[num[i]]=i;        
        }          
           
    return{};       
    }
};
int Main(){
    Solution sol;
    vector<int> num={2,3,4,5,6,7,8,9};
    int target=9;     vector<int>result=sol.twoSum(num,target); 
                cout<<"["<<result[0]<<","<<result[1]<<"]"<<endl;    
return 0;    
};
