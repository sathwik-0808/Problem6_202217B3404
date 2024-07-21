class Queue:
    def __init__(self, size):
        self.size = size
        self.queue = [None] * size
        self.front = -1
        self.rear = -1
 
    def is_full(self):
        return self.rear == self.size - 1
 
    def is_empty(self):
        return self.front == -1 or self.front > self.rear
 
    def enqueue(self, element):
        if self.is_full():
            print("Queue is full")
        else:
            if self.front == -1:
                self.front = 0
            self.rear += 1
            self.queue[self.rear] = element
            self.display()
 
    def dequeue(self):
        if self.is_empty():
            print("Queue is empty")
        else:
            print("Deleted element:", self.queue[self.front])
            for i in range(self.front, self.rear):
                self.queue[i] = self.queue[i + 1]
            self.rear -= 1
            if self.rear < self.front:
                self.front = self.rear = -1
            self.display()
 
    def display(self):
        if self.is_empty():
            print("Queue is empty")
        else:
            print("Queue elements:", self.queue[self.front:self.rear + 1])
 
def main():
    size = int(input("Enter the size of the queue: "))
    q = Queue(size)
    
    while True:
        operation = input("Enter operation (insert/delete/display/exit): ").strip().lower()
        
        if operation == "insert":
            element = input("Enter the element to insert: ")
            q.enqueue(element)
        
        elif operation == "delete":
            q.dequeue()
        
        elif operation == "display":
            q.display()
        
        elif operation == "exit":
            break
        
        else:
            print("Invalid operation. Please enter insert, delete, display, or exit.")
 
if __name__ == "__main__":
    main()