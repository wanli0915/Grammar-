# Grammar

1. Traverse a Linked List
```
  dummy = ListNode()
  pointer = dummy
  
  while xxx:
    ...
    pointer.next = ListNode(5)
    pointer = pointer.next
    ...
  
  return dummy.next
```

2. Python: yield
   
   yield 就是 return 返回一个值，并且记住这个返回的位置，下次迭代就从这个位置后开始
   
   
3. List to string: ','.join(map(str, list))
```
list: [1,2,3]
After ','.join(map(str, list))
We get: '1,2,3'
```

4. defaultdict with int: 
```
defaultdict(lambda: -1)
```

5. Bit Manipulation
```
XOR (^)  = > In short, it means that it returns 1 only if exactly one bit is set to 1 out of the two bits in comparison ( Exclusive OR ).
            A = 5 = 0101, B = 3 = 0011
            A ^ B = 0101 ^ 0011 = 0110 = 6
          = > 有且仅有一个1的时候是1
          = > inequality detector XOR 
          = > n ^ n = 0, n ^ 0 = n
          ！！！满足交换率 顺序不重要 Leetcode136
XNOR  => XNOR gives the reverse of XOR if binary bit. 
      => First bit | Second bit | XNOR  
          0             0           1
          0             1           0
          1             0           0
          1             1           1
          It gives 1 if bits are same else if  
          bits are different it gives 0.
      => equality detector
Left-Shift (<<)  => 把左边的0 delete 加到右边
                 => 1 << 2 -> 100 把001左移两次
                 => 1 << n -> 2^n 把001左移n次
Right-Shift (>>) => 把右边的n位 delete 左边加n个0
                 => 5 >> 1 -> 101 delete 右边的1 左边加个1 -> 010 -> 2
```

6. DP 问题
  * 背包问题: 找到n个数和为capacity, dp[i]表示是否有这样一种可行方案使得元素和为i. [Leetcode416](https://leetcode.com/problems/partition-equal-subset-sum/)
  * 接龙型：[Leetcode368](https://leetcode.com/problems/largest-divisible-subset/)
  * 初始化：
```
  dp = [False] * (capacity + 1)

```

7. 找到一个数所有的factor，这是包括了1和它本身的版本
```
# 用到的方法是对num开根号找factor
# 一个数x的factor可以以sqrt(x)为分界线划分为两半
# 1234|681224 每一个sqrt(x)左边的factor都对应sqrt(x）右边的factor
def get_factors(self, num):
    factor = 1
    factors = []
    while factor * factor <= num:
        if num % factor == 0:
            factors.append(factor)
            # 比如1248，当算到2*2!=8 and 2!=1的时候，append 8//2
            if factor * factor != num:
                factors.append(num // factor)
        factor += 1
    return factors
```

8. Sort
```
# List根据first value sort [[1,3],[2,6],[8,10],[15,18]]
intervals = sorted(intervals, key = lambda interval: interval[0])

# Dict根据value sort 倒序
sorted(d.items(), key=lambda x: x[1], reverse=True)
```

