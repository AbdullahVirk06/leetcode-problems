# leetcode-problems
leetcode repo
class Solution {
public:
    std::vector<int> twoSum(std::vector<int>& nums, int target) {
        // Create an unordered_map to store numbers and their corresponding indices
        std::unordered_map<int, int> numToIndexMap;

        // Loop through the array
        for (int i = 0; i < nums.size(); i++) {
            // Calculate the difference between the target and the current number
            int diff = target - nums[i];

            // Check if the difference already exists in the map
            if (numToIndexMap.find(diff) != numToIndexMap.end()) {
                return {i, numToIndexMap[diff]};
            }

            // If it doesn't exist, add the current number and its index to the map
            numToIndexMap[nums[i]] = i;
        }

        // If no two numbers add up to the target, return an empty vector
        return {};
    }
};
