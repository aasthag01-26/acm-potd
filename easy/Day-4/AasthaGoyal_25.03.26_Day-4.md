class Solution{
public:
    int missingNumber(vector<int> &nums){
        int N = nums.size();
        sort(nums.begin(), nums.end());
        int ans = N;
        for(int i=0; i<N; i++){
            ans ^= nums[i]^i;
        }
        return ans;
    }
}