Explanation of Issue in Calender.py and debugging steps

Limitations and Issues:

The code has a significant flaw in its insert method within the Node class. The conditionals are insufficient to prevent overlapping bookings. It simply tries to insert the new node as a child, not checking for actual overlap completely. For example:
Imagine bookings:

(10, 20)

(15, 25)

The second booking overlaps with the first. However, the code might incorrectly place the second node as a right or left child depending on the order of insertion. This should return False (booking failed), but the implementation is incorrect and could allow overlapping bookings.

To fix the overlapping issue, you'd need to check if the new booking's start is less than the current node's end AND the new booking's end is greater than the current node's start. This condition precisely represents an overlap. Then it should return False
