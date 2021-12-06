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
