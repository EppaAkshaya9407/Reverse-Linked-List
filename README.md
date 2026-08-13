# Reverse-Linked-List
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def reverseList(self, head: Optional[ListNode]) -> Optional[ListNode]:
        if head is None:
           return head
        s=head
        l=None
        while head:
            temp=head.next
            head.next=l
            l=head
            head=temp
        return l
