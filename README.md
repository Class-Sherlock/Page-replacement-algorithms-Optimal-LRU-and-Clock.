# Page-replacement-algorithms-Optimal-LRU-and-Clock.

Paging is the most common implementation of virtual memory. 

Page fault - is an exception raised when a process accesses a memory page that is not currently mapped by MMU, eg. entry in page table marked invalid

When operating system runs out of memory it must replace the pages in an effective manner taking multiple factors into consideration. 

Optimal Algorithm -> replaces the pages that were not used for the longest period of time. It is not very useful as it requires us the know the future. However, it is useful in showing how an optimized algorithm would compare to First come first reverse method. 


Least Recently Used Algorithm (LRU) -> uses the past knowledge to predict the future. replaces the pages based on the frequency of use. If pages don't get used as much compared to others, it will be replaced. 

CLOCK -> Make use of the reference bit in page table entry, which is automatically set by hardware any time page is accessed. frames are organized as a circular buffer. If a page has reference bit = 0, replace it otherwise set reference bit to 0 and advance pointer to the next page
