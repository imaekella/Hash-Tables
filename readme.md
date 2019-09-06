# HASH TABLE

### What is a Hash Table?
⋅⋅* A list-like data structure that’s designed to quickly store and retrieve key data records. 

### Hash Table includes three methods:
..* Search
..* Insert
..* Remove


### Uses of Hash Tables:
..* Hash tables are great in situations where we need to locate and retrieve a record in a collection of millions or billions of entries, for example:
- Accessing records in a database
- Locating items in a computer’s memory
- Spell checkers

### What is Hashing?
..* Hashing refers to the process of taking a key (i.e., a piece of data), scrambling it with a hash function, and producing an index that’s
used to sort the key into a hash table.

### What is a Hash Function?
..* Takes in a key, such as a string or integer, for a data record (often a key-value pair), scrambles it, and outputs an index to be used in a hash table.

### A hash function should:
..* Always return the same output, given the same input
..* Be simple and efficient
..* Distribute values evenly throughout the hash table
..* Avoid collisions (two different inputs =  same output)

### Hash Function Rule:
..* For the same input, it must always generate the same output. Is possible to have two different inputs with the same output. 

### How to resolve a collison? 
..* Open addressing(probing): 
- Jumps to somewhere else in the table to store your key, if the index generated for a key is already taken 

### 3 types of open addressing: 
..* Linear probing: moves one slot to the right until it finds an open index.
..* Quadratic probing: finds an open index by moving one step to the right, then four, then nine, then 16, then 25, etc.
..* Double hashing: uses a secondary hash function to find an open index.

..* Closed addressing(chaining): A method with a more elegant approach to a hash table
implementation.
- Each slot in the hash table is built as a bucket that can hold as many keys as you want.
- If the hash function generates the same index for two keys, we just add them to the bucket. 
- These buckets are implemented as a linked list.



(https://ga-students.slack.com/files/UJAM66X9T/FMS6BGH27/screen_shot_2019-09-06_at_10.23.55_am.png)
(https://ga-students.slack.com/files/UJAM66X9T/FMQSP5C82/screen_shot_2019-09-06_at_10.29.06_am.png)




# QUESTIONS:
1. What are some advantages and disadvantages of Hash Tables?
Advantages
- Fast look up O(1) on average
- Flexible options for keys
Disadvantages
- O(n) lookup in worst case
- Keys are unordered … Looking up a key requires looping through the whole dataset
2. How would you implement chaining for a hash table?
- Make each of the indices in the Hash Table point to a linked list, and when there is a collision add the new value to the end of the linked list.
3. Can you use the same key multiple times for a hash table?
- No. Keys must be unique (i.e. a set) otherwise you’ll only ever be able to retrieve the value from the first instance of the key. Hash indices however can be the same, and should be resolved by chaining or linear probing.
4. What are the pros and cons of chaining vs linear probing?
Chaining:
- Simple insertion and deletion where collisions occur
- Extra data structure (linked list) requires more memory and processing
- Some slots in the table may never get used
Linear Probing
- More processing for insertion and deletion where collisions occur
- Table can be filled up entirely (efficient memory usage) … The flip side of this is that the hash table can be filled up entirely.
- Requires no additional data structures










