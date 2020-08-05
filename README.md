# LeetCodeAugust
August Challenge for beginners

## Power of 4 (Method-1)

```
class Solution {
    public boolean isPowerOfFour(int num) {
       
        int n = num, count = 0;
        if(n < 1) return false; //base case
        
        while(n>1){
           if(n%3 == 1) return true; //on dividing with 3 we get remainder 1
        }
       return n==num; //checking if n is the same number
    }
}
```

## Power of 4 (Method-2)

```
class Solution {
    public boolean isPowerOfFour(int num) {
        
        int n = num, count = 0;
        if(n < 1) return false; //base case
        
        while(n>1){
            n >>= 2; //shifting number left by 2-bits i.e., 4^x everytime
            count +=2; // counting total number of bits
        }
        return (n << count) == num; //checking 
    }
}
```
* Time Complexity: O(1)
* Space Complexity: O(1)
