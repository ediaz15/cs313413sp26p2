TestIterator.java

1) Try with a LinkedList - does it make any difference?
For small values and the operations we do it doesn't seem to have a difference. I guess the concepts of scaling between either or and their tradeoffs become more apparent.
Being said those tradeoffs revolve around arraylists being better for memory but slower due to the operations it does. LinkedLists are better for inserts and deletions but bad for memory as they are moving up the mem hierarchy.

2) What happens if you use list.remove(Integer.valueOf(77))?

We get a concurrentModificationException when we try the Integer.valueOf(77). Im assuming it has to do with the way that iterators are fail-fast.

TestList.java

1) Try with a LinkedList - does it make any difference?
2) What does this method do? [found in the testRemoveObject()]
    a) What does this one do?


TestPerformance.java

1) "TODO Question: What conclusions can you draw about the performance of LinkedList vs. ArrayList when comparing their running times for AddRemove vs. Access? Record those running times in README.txt!"
