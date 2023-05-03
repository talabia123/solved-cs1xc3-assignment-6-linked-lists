Download Link: https://assignmentchef.com/product/solved-cs1xc3-assignment-6-linked-lists
<br>
<ul>

 <li>Write a C program that manipulates linked lists.</li>

</ul>

<strong> </strong>Requirements

As starter code for this assignment, use the C code contained in as6_starter_code.zip file found on Avenue to Learn accompanying this assignment.

This starter code contains the same linked list type used in lectures and labs, and the same set of functions for working with linked lists that we created together in lecture and lab.  The starter code also contains the following function declarations:




// Functions to implement (merge_sorted_lists is a bonus, it is not required) void add_lists(Node *list1, Node *list2);

Node *duplicate_list(Node *head);

Node *efficient_delete_match(Node *head, int delete_value, int *num_deleted);Node *merge_sorted_lists(Node *list1, Node *list2);




This assignment requires you to implement the add_lists, duplicate_list and

efficient_delete_match functions; requirements are described below.  The merge_sorted_lists function is an optional bonus that you can choose to complete or not, it is not required for full marks.  Test code is provided in the main function to help you determine when your function is working correctly, and to clarify any confusion about the requirements provided below.

The function <strong>add_lists</strong> should add the value of each node contained in the same position in the lists together and store the result as the new value of list1’s node at that position.  If list1 is shorter than list2 or vice versa, than for nodes past the shorter of the two lists no addition needs to occur (and list1 should remain the same for these nodes).  Use recursion to create this function (though not required, the function body can be created with 3 lines of code).

The function <strong>duplicate_list</strong> should create a new list on the heap that is a duplicate of the input list provided as an argument.  The duplicate list should have the same number of nodes as the input list, and each node at each position in the list should have the same value as the node in the input list at that position in the input list.  The function should return a pointer to the head of this new list.

The function <strong>efficient_delete_match</strong> should delete any nodes from the list that have a value matching the argument <strong>delete_value</strong> and it should count the number of deletions that have occurred with <strong>num_deleted</strong> (a pass-by-reference parameter).  The function should return a pointer to the (potentially different) head of the resulting list (which could even be NULL/empty).  The function should result in the same resulting list, and same num_deleted value, as the <strong>delete_all_matches</strong> function that we created in-class.

However the <strong>delete_all_matches</strong> function was inefficient… it works by repeatedly calling <strong>delete_first_matc</strong>h until no matches are found.  The delete_first_match function traverses the list until the first match is found, and so if we repeatedly call the function, we are traversing the list again and again.  Your <strong>efficient_delete_match</strong> function should traverse the list <strong>only once</strong>.  You can use multiple loops in your code if like, perhaps traversing a portion of the list, and then another portion of the list, but your code should not repeatedly traverse the same elements of the list.  The <strong>delete_duplicates</strong> function may be helpful as inspiration for how to achieve this.  As a result, the performance should be vastly improved compared to <strong>delete_all_matches</strong>, and test code is provided to demonstrate this.

You can use any of the functions we created in lecture and in lab to help you create the above functions.




<h1>Bonus</h1>

You can optionally create the <strong>merge_sorted_lists</strong> function too for up to 10 bonus marks.  This function should accept two <em>sorted lists</em> as input (sorted from lowest to highest values).  The function should return a pointer to a list that has been created by merging and connecting the nodes in the two lists to form a new list that is also sorted from lowest to highest.  The new list should contain all of the nodes that are in both lists, what should be different is how the nodes point to each other in order to form one merged list.  <strong> </strong>

The function <strong>should not</strong> create any nodes (i.e. create a new list on the heap entirely using the values from the two previous lists).  No new nodes should be created on the heap.  The pointers of the existing lists should be re-arranged to form one new merged list that is ordered from lowest to highest.




<h1>Test Code</h1>

The main function contains test code to test all 4 functions.  You may want to “comment out” this code by surrounding it with /* … */ multiline comments so that you can work on your functions, as the code assumes that all of the functions have been implemented.  You can use this code to help verify that your functions are working correctly.

Note that in the case of merge_sorted_list some random values are used as part of the test, so your results will not be identical.  And in the case of the performance test of the delete functions, the time will be different (but if you’re running the code on the pascal server, a similar very large gap in performance should be evident).

The expected test code results are provided after the mark breakdown, and as a plaintext file on Avenue to Learn accompanying the assignment.


