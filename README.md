Approach

To efficiently handle large files, the program reads the file line by line instead of loading the entire file into memory. This helps process very large datasets without consuming excessive memory.

First, a dictionary (hash map) is used to count how many times each word appears in the file. As each word is read, its frequency is updated in the dictionary.

After counting all frequencies, instead of sorting the entire dataset, a min-heap is used to keep track of only the top 10 most frequent words. The heap maintains the smallest frequency at the top. If a new word has a higher frequency than the smallest element in the heap, it replaces that element. This ensures the heap always contains the most frequent words.

Finally, the heap is sorted in descending order to produce the final output.
