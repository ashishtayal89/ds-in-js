# Basic Datastructures introduced in javascript

- Stack
- Queue
- Linked List
- Tree
- Graph
- Hash Table

## Installation and Usage

```bash
npm install ds-in-js --save-dev
```

### Stack:

```js
const { Stack } = require("ds-in-js");

const stack = new Stack();
stack.push(1);
stack.push(2);
const data = stack.pop(); // 2
const top = stack.peek(); // 1
```

### Queue:

```js
const { Queue } = require("ds-in-js");

const queue = new Queue();
queue.enqueue(1);
queue.enqueue(2);
const data = queue.dequeue(); // 1
const top = queue.peek(); // 2
```

### Linked List

```js
const { LinkedList } = require("ds-in-js");
const lList = new LinkedList([1, 2, 3]);
console.log(lList.getElementAtStart());
```

### Binary Search Tree:

```js
const { BST } = require("ds-in-js");

const bst = new BST();
bst.insert(2);
bst.insert(1);
const node = bst.search(1); // { data: 1, left: null, right: null }
bst.delete(1);
```

### Graph

```js
const { Graph } = require("ds-in-js");
const graph = new Graph();

/*
    a---b
    |  /    
    | /
    c
*/

graph.addVertex("a");
graph.addVertex("b");
graph.addVertex("c");

graph.addEdge("a", "c"); // add weight using graph.addEdge('a', 'c', 10)
graph.addEdge("c", "b");
graph.addEdge("a", "b");

const output = [];
graph.dfs("a", vertex => output.push(vertex.name)); // ['a', 'c', 'b']
```
