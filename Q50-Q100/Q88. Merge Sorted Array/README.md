#### Knowledge used:
1. two pointers

[code](./Solution.js)

#### Complexity:
- Space: `O(1)`, no additional space used
- Time: `O(n)`

#### Mistakes I have made:
1. instead of initializing the counter to iterate through the first array from the
last index `nums1.length - 1`, we should initialize that counter actually from `m + n - 1` in case of length of the first array is longer than `m + n`
so changing
```
let curr = nums1.length - 1;
```
to
```
let curr = m + n - 1;
```
2. 
```
else if (p1 >= 0) {
    nums1[curr--] = nums1[p1--];
}
```
actually it is unnecessary for us to check if the first array still has any remaining, because even if there are some remaining, we just keep them as is and need to do nothing about it