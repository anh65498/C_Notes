## Linked List

NODE *init_list(void);

int insert(NODE *list, char *s); // changed

int delete(NODE *list, char *s); // changed

NODE *find(NODE *list, char *s); // changed

void traverse(NODE *list);

NODE *destroy(NODE *list);       // your task

##### Searching in a Linked List with sentinel node
```c
/***Returns NULL if not found; returns pointer
	to the first element equal to the target value if found.
*/
int *sentinel_search (int  *list, int  list_size, int  target) {
	int *psent = list + list_size;
	int *ploc = list;
    *psent = target;  
// copy target at the end of the list, shorten the condition and fasten the process
	while (target != *ploc)
	   ploc++;
    return ploc == psent ? NULL : ploc;
}

```
