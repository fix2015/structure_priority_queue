# Priority Queue Data Structure in JavaScript 🚀  

A simple implementation of the **Priority Queue** data structure in JavaScript. This repository demonstrates how to create a priority queue class with essential methods and explains its functionality with practical examples.  

---

## What is a Priority Queue?  
A **Priority Queue** is a data structure that stores elements in a way that allows efficient access to the element with the highest priority. Each element in the queue is assigned a priority value, and elements with higher priority are dequeued before elements with lower priority. Priority queues are commonly implemented using heaps.  

---

## Features  
- **Enqueue**: Add an element to the queue with a given priority.  
- **Dequeue**: Remove and return the element with the highest priority.  
- **Peek**: View the element with the highest priority without removing it.  
- **isEmpty**: Check if the queue is empty.  
- **Size**: Get the number of elements in the queue.  

---

## Code Implementation  

Here’s the JavaScript implementation of the priority queue:  

```javascript
class PriorityQueue {
    constructor() {
        this.queue = [];
    }

    // Add an element to the queue with a given priority
    enqueue(element, priority) {
        const item = { element, priority };
        if (this.isEmpty()) {
            this.queue.push(item);
        } else {
            let added = false;
            for (let i = 0; i < this.queue.length; i++) {
                if (item.priority > this.queue[i].priority) {
                    this.queue.splice(i, 0, item);
                    added = true;
                    break;
                }
            }
            if (!added) {
                this.queue.push(item);
            }
        }
    }

    // Remove and return the element with the highest priority
    dequeue() {
        if (this.isEmpty()) {
            return "Queue is empty!";
        }
        return this.queue.shift();
    }

    // View the element with the highest priority without removing it
    peek() {
        if (this.isEmpty()) {
            return "Queue is empty!";
        }
        return this.queue[0];
    }

    // Check if the queue is empty
    isEmpty() {
        return this.queue.length === 0;
    }

    // Get the size of the queue
    size() {
        return this.queue.length;
    }
}
```

---

## Example Usage  

```javascript
// Initialize the priority queue
const pq = new PriorityQueue();

// Enqueue elements with priorities
pq.enqueue("Task 1", 1);
pq.enqueue("Task 2", 3);
pq.enqueue("Task 3", 2);

// Peek at the highest priority element
console.log(pq.peek()); // Output: { element: 'Task 2', priority: 3 }

// Dequeue elements
console.log(pq.dequeue()); // Output: { element: 'Task 2', priority: 3 }
console.log(pq.dequeue()); // Output: { element: 'Task 3', priority: 2 }

// Check if the queue is empty
console.log(pq.isEmpty()); // Output: false

// Get the size of the queue
console.log(pq.size()); // Output: 1
```

---

## Real-World Applications  
1. **Task Scheduling**: Managing tasks based on priority in operating systems.  
2. **Dijkstra's Algorithm**: Finding the shortest path in graphs.  
3. **Job Scheduling**: For scheduling jobs with different priorities in computers.  
4. **Bandwidth Management**: Prioritizing network traffic based on importance.  

---

## TikTok Tutorial 🎥  
Want to see a quick tutorial on how to build this? Check out this TikTok video:  
[]()  

---

## How to Run the Code  
1. Clone the repository:  
   ```bash
   git clone https://github.com/fix2015/structure_priority_queue
   cd structure_priority_queue
   ```
2. Open the file `index.js` in your favorite code editor.  
3. Run the file using Node.js:  
   ```bash
   node index.js
   ```

---

## Contributing  
Contributions are welcome! If you have suggestions or want to add new features, feel free to create a pull request.  

---

## License  
This project is licensed under the MIT License.  

---

## Connect with Me:
- [LinkedIn - Vitalii Semianchuk](https://www.linkedin.com/in/vitalii-semianchuk-9812a786/)
- [Telegram - @jsmentorfree](https://t.me/jsmentorfree) - We do a lot of free teaching on this channel! Join us to learn and grow in web development.
- [Tiktok - @jsmentoring](https://www.tiktok.com/@jsmentoring) Everyday new videos
- [Youtube - @jsmentor-uk](https://www.youtube.com/@jsmentor-uk) Mentor live streams
- [Dev.to - fix2015](https://dev.to/fix2015) Javascript featured, live, experience but about Priority Queue
