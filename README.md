
# Cache page replacement algorithms simulator.

Project developed for Computer Systems discipline - UFF / 2019.  
Developed by: Jacó Julio and Sandro Bonadia.  

## Project description

It's to Build a cached memory page replacement algorithm simulator. The simulator shall receive as input the sequence of references to main memory pages (addresses), and simulate cached substitutions after a miss occurs, for the ** FIFO **, ** LRU **, ** LFU ** and ** RANDOM ** algorithms. The program should take as a parameter the total cache capacity (ie.: total number of pages), the mapping scheme (direct, associative, and associative per set) that the cache will operate, and the name of the input file to be read by the program, containing the sequences of references to memory page accesses. The input file format consists of a memory address value (one integer per line) to be loaded into the program. The simulator output should consist of, for each replacement policy:
- With each new memory reference of the input file, print the list of all pages stored in cache memory;
- At the end of the execution, the amount of hit (* hit *), the amount of failures (* miss *) and the fraction of hits to memory references for each policy.

## Prerequisites

* Languages: Node.js and JavaScript

## Program Execution

To run the program you must use the command:  
`> node app.js`  
  
Passing the following parameters:  

`--filename [ path ]`: Required parameter. It receives as a parameter the path to the .txt file with the memory reference information. This file must contain one integer per line representing the memory references.  

`--size [ number ]`: Required parameter. Receives a numeric value representing the size of cache memory.  

`--mapping [ direct | associative | associative_set ]`: Required parameter. Receives as direct, associative or associative_set values ​​representing the mapping that will be applied to the simulator.  

`--method [ fifo | lru | lfu | random ]`: Required parameter if opting for associative or associative method by set. It receives as value fifo, lru, lfu and random representing the replacement method that will be used by the simulator in case of miss in memory.  

`--sets [ number ]`: Required parameter if opting for associative method per set. It is given a value representing the number of sets that will be divided into memory.  

## Simulator Examples

To run the simulator you must be in the main directory of the program.  

To run the simulator of a size 4 memory and direct mapping:  
`> node app --filename teste01.txt --size 4 --mapping direct`  

To run the simulator of a size 6 memory, with associative mapping and using the LRU method:  
`> node app --filename teste01.txt --size 6 --method lru --mapping associative`  

To run the simulator of a size 4 memory, with two-set associative mapping by set and using the FIFO method:  
`> node app --filename teste01.txt --size 4 --method fifo --mapping associative_set --sets 2`  
