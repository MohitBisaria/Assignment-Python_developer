Explanation of Issue in Calender.py and debugging steps

Limitations and Issues:

The code has a significant flaw in its insert method within the Node class. The conditionals are insufficient to prevent overlapping bookings. It simply tries to insert the new node as a child, not checking for actual overlap completely. For example:
