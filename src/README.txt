COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		No, with respect to testing.

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			Removes the value in list at index 5.

		list.remove(Integer.valueOf(5)); // what does this one do?

			Removes the value 5 from list.

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			The first item in the list of value 77 will be removed each time the wrapping condition passes as i is iterated over.

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.

	SIZE 10
        testArrayListAddRemove:  32 33 34 34 32 33
        testLinkedListAddRemove: 14 13 14 14 13 13
	testArrayListAccess:     09 08 09 08 08 08
        testLinkedListAccess:    10 09 10 09 09 09

	SIZE 100
        testArrayListAddRemove:  36 35 34 33 35 40
        testLinkedListAddRemove: 14 14 13 15 14 14
	testArrayListAccess:     08 09 09 08 09 09
        testLinkedListAccess:    16 15 15 14 15 14

	SIZE 1000
        testArrayListAddRemove:  058 065 065 060 060 058
        testLinkedListAddRemove: 014 013 013 014 013 013
	testArrayListAccess:     009 009 009 008 009 009
        testLinkedListAccess:    163 164 165 172 164 163

	SIZE 10000
        testArrayListAddRemove:  276 272 276 276 275 273
        testLinkedListAddRemove: 016 015 015 016 015 017
	testArrayListAccess:     009 009 009 009 009 010
        testLinkedListAccess:    866 890 860 874 872 832

	listAccess - which type of List is better to use, and why?

		ArrayList; CPU can much more quickly traverse memory by index instead of by chained object reference.

	listAddRemove - which type of List is better to use, and why?

		LinkedList; index-based removal is faster on LinkedList, where only pointers need to be changed to re-order the list.
