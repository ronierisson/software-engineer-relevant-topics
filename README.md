# Software Engineer Relevant Topics

## Data Structures

<details markdown="1">
<summary>What Are Data Structures?</summary>
<p align="left">
Data structure, way in which data are stored for efficient search and retrieval. Different data structures are suited for different problems. 
Some data structures are useful for simple general problems, such as retrieving data that has been stored with a specific identifier. 
For example, an online dictionary can be structured so that it can retrieve the definition of a word.
On the other hand, specialized data structures have been devised to solve complex specific search problems.

![Logarithm](./img/data-structures.jpeg)

</p>

</details>

<details markdown="1">
<summary>Complexity Analysis</summary>
<p align="left">
Complexity analysis is a way of estimating how much time or space will be used by the algorithm to process large amounts of data. This is done by bounding the behavior above or below by constant multiples of simple functions of the amount of data. Often these are a simple power, like the square, or a logarithm, or the product of the two. Sometimes they are faster growing functions, like 2 to the n.
Sometimes you look at average behavior, sometimes worst case or even best case.
This has come up for me many times, as a way to evaluate approaches, or tune disasterously slow processes. Moving to a new algorithm that had a lower complexity once turned 30 hours of processing increasing rapidly as we got more data to 15 minutes growing slowly. Factor of 100 improvements like that are pretty common.
There are worse cases where time or space grow so fast that only tiny amounts of data can be processed at all.
</p>
</details>

<details markdown="1">
<summary>Memory</summary>
<p align="left">
Simply memory allocation means: 
<br>Reserving memory for specific purposes.
<br>Programs and services are assigned with a specific memory as per their requirements when they are executed. Once the program has finished its operation , the memory is released and allocated to another program or merged within the primary memory.
<br><br>Memory allocation has of two types :
<br>Static Memory Allocation: The program is allocated memory at compile time.
<br>Dynamic Memory Allocation: The programs are allocated with memory at run time.
</p>
</details>

<details markdown="1">
<summary>Big O Notation</summary>

![Big-O](./img/big-o.png)

Below are the Big O performance of common functions of different Java Collections.

#### Complexity (Good to Bad)
| Performance | Notation                                       |
|-------------|------------------------------------------------|
| Good        | <span style="color:#01e703;">O(1)</span>       |
| Good        | <span style="color:#01e703;">O(log n)</span>   |
| Fair        | <span style="color:#e0b20f;">O(n)</span>       |
| Bad         | <span style="color:#fc1d52;">O(n log n)</span> |
| Bad         | <span style="color:#fc1d52;">O(n^2)</span>     |
| Bad         | <span style="color:#fc1d52;">O(2^n)</span>     |
| Bad         | <span style="color:#fc1d52;">O(n!)</span>      |


| List                 | Add                                      | Remove                                   | Get                                      | Contains                                 | Next                                     | Data Structure |
|----------------------|------------------------------------------|------------------------------------------|------------------------------------------|------------------------------------------|------------------------------------------|----------------|
| ArrayList            | <span style="color:#01e703;">O(1)</span> | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | Array          |
| LinkedList           | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | Linked List    |    
| CopyOnWriteArrayList | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | Array          |   

Note: h is the table capacity

| Set                   | Add                                          | Remove                                       | Contains                                     | Next                                         | Size                                     | Data Structure           |
|-----------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|------------------------------------------|--------------------------|
| HashSet               | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | O(h/n)                                       | <span style="color:#01e703;">O(1)</span> | Hash Table               |
| LinkedHashSet         | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span> | Hash Table + Linked List |
| EnumSet               | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span> | Bit Vector               |
| TreeSet               | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(1)</span> | Red-black tree           |
| CopyOnWriteArraySet   | <span style="color:#e0b20f;">O(n)</span>     | <span style="color:#e0b20f;">O(n)</span>     | <span style="color:#e0b20f;">O(n)</span>     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span> | Array                    |
| ConcurrentSkipListSet | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(1)</span>     | <span style="color:#e0b20f;">O(n)</span> | Skip List                |

| Queue                   | Offer                                        | Peak                                     | Poll                                         | Remove                                   | Size                                     | Data Structure |  
|-------------------------|----------------------------------------------|------------------------------------------|----------------------------------------------|------------------------------------------|------------------------------------------|----------------|
| PriorityQueue           | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | Priority Heap  |
| LinkedList              | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> | Array          |
| ArrayDequeue            | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span>     | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | Linked List    |
| ConcurrentLinkedQueue   | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span>     | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> | Linked List    |
| ArrayBlockingQueue      | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span>     | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | Array          |
| PriorirityBlockingQueue | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | Priority Heap  |
| SynchronousQueue        | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span>     | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | None!          |
| DelayQueue              | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | Priority Heap  |
| LinkedBlockingQueue     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span>     | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#01e703;">O(1)</span> | Linked List    |

Note: h is the table capacity

| Map                   | Get                                          | ContainsKey                                  | Next                                         | Data Structure           |
|-----------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|--------------------------|
| HashMap               | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | O(h / n)                                     | Hash Table               |
| LinkedHashMap         | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | Hash Table + Linked List |
| IdentityHashMap       | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | O(h / n)                                     | Array                    |
| WeakHashMap           | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | O(h / n)                                     | Hash Table               |
| EnumMap               | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | Array                    |
| TreeMap               | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> | Red-black tree           |
| ConcurrentHashMap     | <span style="color:#01e703;">O(1)</span>     | <span style="color:#01e703;">O(1)</span>     | O(h / n)                                     | Hash Tables              |
| ConcurrentSkipListMap | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(1)</span>     | Skip List                |
</details>

<details markdown="1">
<summary>Logarithm</summary>
<p align="left">
The binary logarithm function may be defined as the inverse function to the power of two function, which is a strictly increasing function over the positive real numbers and therefore has a unique inverse. 
<br>Alternatively, it may be defined as ln n/ln 2, where ln is the natural logarithm, defined in any of its standard ways. 
<br>Using the complex logarithm in this definition allows the binary logarithm to be extended to the complex numbers.

As with other logarithms, the binary logarithm obeys the following equations, which can be used to simplify formulas that combine binary logarithms with multiplication or exponentiation:

![Logarithm](./img/logarithm.png)

</p>
</details>


<details markdown="1">
<summary>Arrays</summary>

[Arrays - Java Documentation](https://docs.oracle.com/javase/8/docs/api/java/util/Arrays.html)

|  Action   |                 Average                  |                  Worst                   |
|:---------:|:----------------------------------------:|:----------------------------------------:|
|  Access   | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> |
|  Search   | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Deletion  | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|
</details>


<details markdown="1">
<summary>Linked Lists</summary>

[Linked Lists - Java Documentation](https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html)

#### Singly-Linked List
|  Action   |                 Average                  |                  Worst                   |
|:---------:|:----------------------------------------:|:----------------------------------------:|
|  Access   | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |
|  Search   | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> |
| Deletion  | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|

#### Doubly-Linked List
|  Action   |                 Average                  |                  Worst                   |
|:---------:|:----------------------------------------:|:----------------------------------------:|
|  Access   | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |
|  Search   | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> |
| Deletion  | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|

#### Skip List
|  Action   |                   Average                    |                  Worst                   |
|:---------:|:--------------------------------------------:|:----------------------------------------:|
|  Access   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
|  Search   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Deletion  | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |

| Space Complexity | <span style="color:#fc1d52;">O(n log n)</span> |
|:----------------:|:----------------------------------------------:|
</details>

<details markdown="1">
<summary>Hash Tables</summary>

[Hash Tables - Java Documentation](https://docs.oracle.com/javase/8/docs/api/java/util/Hashtable.html)

|  Action   |                 Average                  |                  Worst                   |
|:---------:|:----------------------------------------:|:----------------------------------------:|
|  Access   |                   N/A                    |                   N/A                    |
|  Search   | <span style="color:#01e703;">O(1)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#01e703;">O(1)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Deletion  | <span style="color:#01e703;">O(1)</span> | <span style="color:#e0b20f;">O(n)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|
</details>

<details markdown="1">
<summary>Stacks</summary>

[Stacks - Java Documentation](https://docs.oracle.com/javase/8/docs/api/java/util/Stack.html)

|  Action   |                 Average                  |                  Worst                   |
|:---------:|:----------------------------------------:|:----------------------------------------:|
|  Access   | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |
|  Search   | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> |
| Deletion  | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|
</details>

<details markdown="1">
<summary>Queues</summary>

[Queues - Java Documentation](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html)

|  Action   |                 Average                  |                  Worst                   |
|:---------:|:----------------------------------------:|:----------------------------------------:|
|  Access   | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |
|  Search   | <span style="color:#e0b20f;">O(n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> |
| Deletion  | <span style="color:#01e703;">O(1)</span> | <span style="color:#01e703;">O(1)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|
</details>

<details markdown="1">
<summary>Strings</summary>

[Strings - Java Documentation](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)

[Strings - Baeldung](https://www.baeldung.com/java-string)

</details>

<details markdown="1">
<summary>Graphs</summary>

[Graphs - Baeldung](https://www.baeldung.com/java-graphs)

</details>

<details markdown="1">
<summary>Trees</summary>

[Trees - Java Documentation](https://docs.oracle.com/javase/8/docs/api/javax/swing/tree/TreeNode.html)

#### B-Tree
|  Action   |                   Average                    |                  Worst                   |
|:---------:|:--------------------------------------------:|:----------------------------------------:|
|  Access   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
|  Search   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Deletion  | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|

#### Cartesian Tree
|  Action   |                   Average                    |                  Worst                   |
|:---------:|:--------------------------------------------:|:----------------------------------------:|
|  Access   |                     N/A                      |                   N/A                    |
|  Search   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Deletion  | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|

#### B+ Tree
|  Action   |                   Average                    |                    Worst                     |
|:---------:|:--------------------------------------------:|:--------------------------------------------:|
|  Access   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |
|  Search   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |
| Insertion | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |
| Deletion  | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|

#### Red-Black Tree
|  Action   |                   Average                    |                    Worst                     |
|:---------:|:--------------------------------------------:|:--------------------------------------------:|
|  Access   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |
|  Search   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |
| Insertion | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |
| Deletion  | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|

#### Splay Tree
|  Action   |                   Average                    |                  Worst                   |
|:---------:|:--------------------------------------------:|:----------------------------------------:|
|  Access   |                     N/A                      |                   N/A                    |
|  Search   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Deletion  | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|

#### AVL Tree
|  Action   |                   Average                    |                    Worst                     |
|:---------:|:--------------------------------------------:|:--------------------------------------------:|
|  Access   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |
|  Search   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |
| Insertion | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |
| Deletion  | <span style="color:#01e703;">O(log n)</span> | <span style="color:#01e703;">O(log n)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|

#### KD Tree
|  Action   |                   Average                    |                  Worst                   |
|:---------:|:--------------------------------------------:|:----------------------------------------:|
|  Access   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
|  Search   | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Insertion | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |
| Deletion  | <span style="color:#01e703;">O(log n)</span> | <span style="color:#e0b20f;">O(n)</span> |

| Space Complexity | <span style="color:#e0b20f;">O(n)</span> |
|:----------------:|:----------------------------------------:|
</details>

## Systems Design Fundamentals

<details markdown="1">
<summary>Client Server Model</summary>
<p align="left">
<strong>What is a Client?</strong>

A client is a computer hardware device or software that accesses a service made available by a server. The server is often (but not always) located on a separate physical computer.

<strong>What is a Server?</strong>

A server is a physical computer dedicated to run services to serve the needs of other computers. Depending on the service that is running, it could be a file server, database server, home media server, print server, or web server.
<br>

![Client <-> Server](./img/client_server.png)

</p>
</details>

<details markdown="1">
<summary>Network Protocols</summary>
<p align="left">

![Network Protocols](./img/network_protocols.png)

![Network Layers](./img/network_layers.png)

![Network Ports](./img/network_ports.png)

[Network Protocols - Baeldung](https://www.baeldung.com/cs/popular-network-protocols)

</p>
</details>

<details markdown="1">
<summary>Storage</summary>
<p align="left">

PostgreSQL example<br>

![Storage](./img/storage.png)

</p>
</details>

<details markdown="1">
<summary>Latency And Throughput</summary>
<p align="left">

Latency is the time required to perform some action or to produce some result. Latency is measured in units of time -- hours, minutes, seconds, nanoseconds or clock periods.

<br>Throughput is the number of such actions executed or results produced per unit of time. This is measured in units of whatever is being produced (cars, motorcycles, I/O samples, memory words, iterations) per unit of time. The term "memory bandwidth" is sometimes used to specify the throughput of memory systems.
<br>![Latency And Throughput](./img/latency_and_throughput.jpg)

</p>
</details>

<details markdown="1">
<summary>Availability</summary>
<p align="left">

![Availability](./img/availability.jpeg)

</p>
</details>

<details markdown="1">
<summary>Caching</summary>
<p align="left">

![Cache](./img/cache.png)

</p>
</details>

<details markdown="1">
<summary>Proxies</summary>
<p align="left">

![Proxy](./img/proxy.png)

NGINX Reverse Proxy 
<br>![NGINX Reverse Proxy](./img/proxy_nginx.png)

</p>
</details>

<details markdown="1">
<summary>Load Balancers</summary>
<p align="left">

![Load Balancer](./img/load_balancer.jpg)

![Load Balancer Strategies](./img/load_balancer_strategies.jpg)

![API Gateway](./img/api-gateway.png)

</p>
</details>

<details markdown="1">
<summary>Hashing</summary>
<p align="left">

![Consistent Hashing](./img/consistent-hashing.jpeg)

[What is Consistent Hashing and Where is it used?](https://www.youtube.com/watch?v=zaRkONvyGr8)

[Learn hashing and consistent hash ring](https://www.youtube.com/watch?v=bBK_So1u9ew)

</p>
</details>

<details markdown="1">
<summary>Relational Databases</summary>
<p align="left">

![Relational Databases](./img/relational-database.png)

![SQL](./img/sql.jpg)

![Basic SQL](./img/sql-basic.png)

![Notation](./img/notation.png)

</p>
</details>

<details markdown="1">
<summary>Key-Value Stores</summary>
<p align="left">

![Key - Value](./img/key-value-data-stores.png)

[Redis](https://redis.io/) is a good example of key-value store
<br>![Redis](./img/redis.jpg)

</p>
</details>

<details markdown="1">
<summary>Specialized Storage Paradigms</summary>
<p align="left">

Blob Storages: Google Cloud Storage or S3
<br>Time Series Database: InfluxDB or Prometheus
<br>Graph Database: Neo4j cypher language
<br>Spatial Database: Quadtree

</p>
</details>

<details markdown="1">
<summary>Replication And Sharding</summary>
<p align="left">

Database sharding:
<br>![Database Sharding](./img/database-sharding.jpg)

![Database Sharding](./img/shards.png)

Database scale:
<br>![Database Scale](./img/scalable-postgresql.png)

![Database Read and Write Scale](./img/loadbalancer-read-and-write-application-auto-scaling.png)

![Database Read and Write](./img/db-read-and-write.png)

</p>
</details>

<details markdown="1">
<summary>Leader Election</summary>
<p align="left">

Zookeeper:
<br>![Database Read and Write](./img/leader-election-zookeeper.png)

![Database Read and Write](./img/zookeeper.jpg)

</p>
</details>

<details markdown="1">
<summary>Peer-To-Peer Networks</summary>
<p align="left">

![Peer-To-Peer Networks](./img/p2p.png)

</p>
</details>

<details markdown="1">
<summary>Polling And Streaming</summary>
<p align="left">

![Polling And Streaming](./img/polling-streaming.png)

[Polling And Streaming - Explanation](https://www.youtube.com/watch?v=rHOHOt7oz-4)

</p>
</details>

<details markdown="1">
<summary>Configuration</summary>
<p align="left">

![config](./img/config.jpeg)

</p>
</details>

<details markdown="1">
<summary>Rate Limiting</summary>
<p align="left">

![Rate Limit](./img/rate-limit.png)

[Secure Rate Limiting with Spring Cloud Gateway](https://piotrminkowski.com/2021/05/21/secure-rate-limiting-with-spring-cloud-gateway/)

![Rate Limit With Spring Cloud](./img/spring-cloud-gateway-secure-rate-limiter.png)

</p>
</details>

<details markdown="1">
<summary>Logging And Monitoring</summary>
<p align="left">

Splunk:
<br>![Splunk](./img/splunk.png)

Splunk alert to Slack
<br>![Splunk Alert To Slack](./img/splunk-alert-to-slack.jpeg)

Grafana:
<br>![Grafana](./img/grafana.png)

</p>
</details>

<details markdown="1">
<summary>Publish/Subscribe Pattern</summary>
<p align="left">

![Publish/Subscribe Pattern](./img/publish-subscribe-pattern.png)

Spring Kafka:
<br>![Spring Kafka](./img/spring-kafka.png)
</p>
</details>

<details markdown="1">
<summary>MapReduce</summary>
<p align="left">

![MapReduce](./img/map-reduce.jpg)

[Hadoop](https://hadoop.apache.org/)

[MapReduce whitepaper](https://static.googleusercontent.com/media/research.google.com/pt-BR//archive/mapreduce-osdi04.pdf)

[MapReduce - Computerphile](https://www.youtube.com/watch?v=cvhKoniK5Uo)

</p>
</details>

<details markdown="1">
<summary>Security And HTTPS</summary>
<p align="left">

HTTP and HTTPS:
<br>![HTTP and HTTPS](./img/http-and-https.png)

![HTTP and HTTPS diagram](./img/http-vs-https-comparison-diagram.png)

SSL and TLS handshake process:
<br>![SSL and TLS handshake process](./img/ssl-tls-handshake-process.png)

SSL and TLS history:
<br>![SSL and TLS history](./img/ssl-tls.png)

SSL and TLS:
<br>![SSL and TLS Diff](./img/ssl-and-tls-diff.png)

</p>
</details>

<details markdown="1">
<summary>API Design</summary>
<p align="left">

Spring:
<br>![Spring](./img/spring-design-api.png)

![Spring](./img/spring.png)


Endpoints:
<br>![Endpoints](./img/endpoints.png)

</p>
</details>