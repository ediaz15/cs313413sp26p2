TestIterator.java

1) Try with a LinkedList - does it make any difference?
For small values and the operations we do it doesn't seem to have a difference. I guess the concepts of scaling between either or and their tradeoffs become more apparent.
Being said those tradeoffs revolve around arraylists being better for memory but slower due to the operations it does. LinkedLists are better for inserts and deletions but bad for memory as they are moving up the mem hierarchy.

2) What happens if you use list.remove(Integer.valueOf(77))?

We get a concurrentModificationException when we try the Integer.valueOf(77). Im assuming it has to do with the way that iterators are fail-fast.

TestList.java

1) Try with a LinkedList - does it make any difference?
A LinkedList implementation of the tests seem to have a slower runtime on average than the arraylist. Though it could be through the methods we are using to test it.
Maybe it was just the few times that I tried it that it seem to happen for this. Being said, as the previoous question from the other file, I think the tradeoffs still appear under the hood.

2) What does this method do? [found in the testRemoveObject()]
    The list.remove() here is using the integer we passed to it to go to that index of said list and remove the element there

    a) What does this one do?
    in this one while we are using another integer that we passed to it, it looks for the first value of 5 then removes it?

TestPerformance.java

1) "TODO Question: What conclusions can you draw about the performance of LinkedList vs. ArrayList when comparing their running times for AddRemove vs. Access? Record those running times in README.txt!"
INCREASED REPS (REPS = 10000000, SIZE = 10)
ArrayList takes longer than LinkedLists for adding and removing elements.
Around the same for general element access.

INCREASED SIZE((REPS = 10, SIZE = 10000000)
*had to decrease size by / 10 for linkedlist to work*
on average same time for adding and removing BUT LinkedList triggered a heap space error for LinkedLists when doing the original size
Arraylist had worked still.
General same access time for both arraylist and linkedlist.

BOTH SIZE AND REPS = 1000000

LinkedList is way faster than arraylist for adding and removing elements
(1s avg linkedlist VS 10+ sec avg arraylist)

ArrayList is faster than linkedlist for accessing elements

Nice the tradeoffs are apparant when working with data structures!