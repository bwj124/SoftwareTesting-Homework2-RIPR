```
public int findLast (int[] x, int y) {
    //Effects: If x==null throw NullPointerException 
    // else return the index of the last element    
    // in x that equals y. 
    // If no such element exists, return -1
    for (int i=x.length-1; i > 0; i--) 
    { 
        if (x[i] == y) 
        {
            return i; 
        }
     }
    return -1; 
}
// test: x=[2, 3, 5]; y = 2
// Expected = 0
```
(1) 导致错误的根本原因是当x长度为1时，不进入循环，直接导致返回-1，而不是正确的索引值i。

(2) test: x = []; y = 3	expected = -1

(3) test: x = [1]; y = 1	expected = 0

(4) test: x = null; y = 1	expected = NullPointerException.class

```
public static int lastZero (int[] x) {
    //Effects: if x==null throw NullPointerException
    // else return the index of the LAST 0 in x.
    // Return -1 if 0 does not occur in x
    for (int i = 0; i < x.length; i++)
    {
         if (x[i] == 0)
        {
              return i;
         } 
     } return -1;
}
// test: x=[0, 1, 0]
// Expected = 2
```
(1) 导致错误的根本原因是，想要寻找的是最后一个0，但是按照现在的代码逻辑寻找到的是第一个0

(2) test: x = []		expected = -1

(3) test: x = [0, 0, 0]		expected = 2

(4) test: x = null		expected = NullPointerException.class

