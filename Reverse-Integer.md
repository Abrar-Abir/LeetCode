# Reverse Integer

Given a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-2^(31), 2^(31) - 1], then return 0.

Assume the environment does not allow you to store 64-bit integers (signed or unsigned).

 

Example 1:
```
Input: x = 123
Output: 321
```
Example 2:
```
Input: x = -123
Output: -321
```
Example 3:
```
Input: x = 120
Output: 21
```
Example 4:
```
Input: x = 0
Output: 0
```

Constraints:

-2^(31) <= x <= 2^(31) - 1

### Solution

```
class Solution:
    def reverse(self, x: int) -> int:
        y = int(str(abs(x))[::-1])
        return y*( y >= -2**(31) and y < 2**(31))*(-1)**(x < 0)
```
