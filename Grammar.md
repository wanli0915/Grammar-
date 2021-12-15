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
