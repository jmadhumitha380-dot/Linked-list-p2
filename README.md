# Linked-list-p2
Practice program
class Node:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks
        self.next = None
class LinkedList:
    def __init__(self):
        self.head = None
    def add_student(self, name, marks):
        new_node = Node(name, marks)
        if self.head is None:
            self.head = new_node
        else:
            temp = self.head
            while temp.next:
                temp = temp.next
            temp.next = new_node
    def display(self):
        temp = self.head
        while temp:
            print("Name:", temp.name, "Marks:", temp.marks)
            temp = temp.next
ll = LinkedList()
ll.add_student("Arun", 85)
ll.add_student("Bala", 90)
ll.add_student("Cathy", 78)
print("Student Records:")
ll.display()

Output:
Output:
Student Records:
Name: Arun Marks: 85
Name: Bala Marks: 90
Name: Cathy Marks: 78
