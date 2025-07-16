// Linked list - Singly

class Node {
    int value;
    Node next;

    // constructor
    Node(int value) {
        this.value = value;
        this.next = null;
    }
}

public class SLL {

    Node head;

    // SLL constructor to initialize an empty list
    public SLL() {
        this.head = null;
    }

    // InsertAtBeginning
    public void InsertAtBeginning(int value) {
        Node newNode = new Node(value);
        newNode.next = head;
        head = newNode;
    }

    // insertatEnd
    public void InsertAtEnd(int value) {
        Node newNode = new Node(value);
        // Handle case for an empty list: new node becomes the head
        if (head == null) {
            head = newNode;
            return;
        }
        Node temp = head;
        while (temp.next != null) {
            temp = temp.next;
        }
        temp.next = newNode;
    }

    // insertAtSpecific Position
    public void insertAtSpecificPosition(int value, int position) {
        if (position < 1) {
            System.out.println("Invalid position");
            return;
        }

        if (position == 1) {
            InsertAtBeginning(value);
            return;
        }

        Node temp = head;
        Node newNode = new Node(value);
        // Traverse to the node just before the desired position
        // For position 'n', loop to (n-1)th node
        for (int i = 1; temp != null && i < position - 1; i++) {
            temp = temp.next;
        }

        if (temp == null) {
            System.out.println("Position out of Range");
            return;
        } else {
            newNode.next = temp.next; // New node points to current temp's next
            temp.next = newNode;       // Temp points to new node
        }
    }

    // deleteatbeg
    public void deleteatbeg() {
        if (head == null) { // Handle case for empty list
            // System.out.println("List is empty, cannot delete from beginning.");
            return;
        }
        head = head.next;
    }

    // deleteatend
    public void deleteatend() {
        if (head == null) { // Handle case for empty list
            // System.out.println("List is empty, cannot delete from end.");
            return;
        }
        if (head.next == null) { // Handle case for a single node list
            head = null;
            return;
        }
        Node temp = head;
        // Traverse until temp.next is the last node
        // (i.e., temp.next.next is null, so temp is the second-to-last node)
        while (temp.next.next != null) {
            temp = temp.next;
        }
        temp.next = null; // Cut off the last node
    }

    // display method
    public void display() {
        Node temp = head;
        if (temp == null) {
            System.out.println("List is empty"); // Indicate empty list
            return;
        }
        while (temp != null) {
            System.out.print(temp.value + " -> ");
            temp = temp.next;
        }
        System.out.println("null"); // Use println to move to the next line after display
    }

    public static void main(String[] args) {

        SLL list = new SLL(); // Create a new instance of your SLL

        System.out.println("--- Initial insertions at beginning ---");
        list.InsertAtBeginning(5);
        list.display();
        list.InsertAtBeginning(15);
        list.display();
        list.InsertAtBeginning(25);
        list.display();
        list.InsertAtBeginning(35);
        list.display(); // Expected: 35 -> 25 -> 15 -> 5 -> null

        System.out.println("\n--- Insertions at end ---");
        list.InsertAtEnd(50);
        list.display();
        list.InsertAtEnd(60);
        list.display();
        list.InsertAtEnd(70);
        list.display(); 
        
        System.out.println("\n--- Inserting at specific position (value 42 at position 3) ---");
        list.insertAtSpecificPosition(42, 3);
        list.display(); 
        
        System.out.println("\n--- Deleting from end ---");
        list.deleteatend();
        list.display();

        System.out.println("\n--- Deleting from beginning ---");
        list.deleteatbeg();
        list.display();

        System.out.println("\n--- Final list state ---");
        list.display();
    }
}
