Download Link: https://assignmentchef.com/product/solved-col216-assignment12-simulating-cache-memory
<br>
[Substitute for Major examination]

You will be awarded marks according to your design and the test cases you developed to evaluate the design. Extensive testing is expected as a part of the Assignment

In this assignment you will develop a simulation software for cache memory. The simulated cache will have the functionality that was discussed in the cache memory lecture videos, but with a <em>new Replacement Policy</em> that works as follows. Each Cache Set is divided into two groups:

<ol>

 <li>One group contains the HIGH PRIORITY lines of the set</li>

 <li>The other group contains the LOW PRIORITY lines of the set</li>

</ol>

How is <em>priority</em> established? If a line is accessed again after the initial access that fetches it into the cache, it is promoted to the HIGH PRIORITY group. If a line is not accessed for sufficiently long (T cache accesses) after being moved to the HIGH PRIORITY group, it is moved to the LOW PRIORITY group. Within a priority group, the Least Recently Used policy may be used to manage the lines.

Make any reasonable assumptions you need. The above priority scheme is just an outline; it may not be complete. Feel free to add other details to make this work.

<strong>Inputs</strong> to the software will be: (inputs to be taken from input file)

<ol>

 <li>Cache size</li>

 <li>Cache line/block size</li>

 <li>Cache associativity</li>

 <li>The value of T</li>

 <li>A sequence of memory access requests: Memory address, R or W (for Read or Write), and Data (if Write)</li>

</ol>

<strong>Outputs</strong> from the software will be: (output the content and cache statistics to output file)

<ol>

 <li>The complete content of the cache (Data, Tag, and Control bits of every cache line) in each Way after the memory access sequence is complete.</li>

 <li>Cache statistics:

  <ol>

   <li>Number of Accesses</li>

   <li>Number of Reads, Read Hits, and Read Misses</li>

   <li>Number of Writes, Write Hits, and Write Misses</li>

   <li>Hit Ratio</li>

  </ol></li>

</ol>

<strong>Deliverables</strong>:

<ol>

 <li>Software implementation of the cache described above</li>

 <li>Document describing the design. In the document, discuss your implementation of the replacement policy. Are the High and Low priority groups fixed in size? That is, in an 8way associative cache, are there 4 high-priority and 4 low-priority groups? Or some other break-up? Why? Can these sizes change at runtime?</li>

</ol>

<strong>Sample Input File</strong>:

Considered a very small cache size for demonstrating sample input and sample output. You are expected to consider different cache sizes and configurations.

Assumptions made :

<ol>

 <li>Out of 2 ways for each set, one way is assigned to high priority group and second way is assigned to low priority group.</li>

 <li>When valid status of the line is being modified to invald, the dirty status is left unmodified.</li>

</ol>

When a line is being made invalid, modifying the dirty status is upto the implementation choice.


