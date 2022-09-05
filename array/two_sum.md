this is easy question to search 2 numbers on array that have same sum as target
- brute force technique with on2
```
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    for (let i = 0; i < nums.length; i++) {
        for (let j = i + 1; j < nums.length; j++) {
            if (nums[i] + nums[j] === target) {
                return [i, j]
            }
        }
    }
};
```

- use hashmap tecnique to check index of array with oN
```
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    let map = {}
    for(let i = 0; i<nums.length; i++) {
        map[nums[i]] = i
        if(map[target - nums[i]] !== undefined) {
            return [map[target -nums[i]], i]
        }
    }
};
```
