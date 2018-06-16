## Heapq for Typescript

Heap queue algorithm implementation for Typescript based on heapq.py module from CPython

### Installation

    npm install ts-heapq
    
### Use
#### Simple example
    import { Heapq } from "ts-heapq";
    
    let heap: Heapq<number> = new Heapq<number>();
    heap.push(3);
    heap.push(1);
    heap.push(2);
    
    heap.top(); // return 1;
    heap.pop(); // return 1, heap contains [2, 3];
    heap.top(); // returns 2;
    
#### Implementing max heap using custom comparator
    import { Heapq } from "ts-heapq";
    
    let maxHeap: Heapq<number> = new Heapq<number>([], comparator: (a: number, b: number) => a > b);
    maxHeap.push(1);
    maxHeap.push(3);
    maxHeap.push(2);
    
    maxHeap.top(); // return 3;
    maxHeap.pop(); // return 3, heap contains [2, 1];
    maxHeap.top(); // returns 2;