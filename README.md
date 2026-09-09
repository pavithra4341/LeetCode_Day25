# 25. Reverse Nodes in k-Group

## Problem
Reverse linked list in groups of `k`. If nodes left < k, leave as is.

Ex: [1,2,3,4,5], k=2 -> [2,1,4,3,5]

## Approach - In-place Reversal O(1) Space

1. `dummy -> head` to handle edge cases
2. Loop groups:
   - Find kth node from `group_prev`. If not found -> done
   - Save `group_next = kth.next`
   - Reverse k nodes between `group_prev.next` and `group_next`
   - Reconnect: `group_prev.next = kth`, `group_prev = old_head`

## Complexity
Time: O(n)
Space: O(1)
