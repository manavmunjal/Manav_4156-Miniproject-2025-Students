Documentation for list of bugs found -
1) Changed names and references of classes BOOK to Book, BOOKUnitTests to BookUnitTests and MockAPIService to MockApiService respectively.
2) deleteCopy method of Book.java had a logical bug and we had to replace true and false return positions for it to logically work.
3) addCopy method of Book.java had an empty catch block and I added logic to it and accordingly wrote tests for the same.
4) checkoutCopy method of Book.java had a logical bug where we were intially decreasing the amountOfTimesCheckedOut on every checkout. I corrected the logic and incremented it on every checkout.
5) returnCopy method of Book.java checked list contents only if list was empty which is again a logical error and I fixed the logic by ensuring it checks only when list is not empty.
6) getLanguage method of Book.java was empty so I corrected the logic and returned the language inside it.
7) setShelvingLocation method of Book.java was always returning the string "shelvingLocation" instead of the value of variable shelvingLocation. I corrected that bug.
8) As a part of exercise 0, the bug in Book.java was that obj of type Object was getting assigned to cmpBook of class Book without being typecasted. So I corrected it to Book cmpBook = (Book) obj;
9) The second bug of exercise 0 was that addCopy of RouteController.java was missing a return statement which was originally inside the try statement. I placed it at the correct position for the function to always have a default return.
10) I had to reposition the imports in a lexicographical order in all the files
11) I gave the appropriate comments where they were missing to explain what the controller does and what the mockapiservice does in RouteController.java
12) getAvailableBooks in RouteContoller.java had indentation errors in availableBooks arrayList creation which I corrected.
13) I made similar indentation changes, filled the catch block with code and kept a default return for addCopy method of RouteController class.
14) MockApiService - line 65 - this.books is assigned to this.books itself instead of updating with tmpBooks.
15) RouteController.java - line 63 - For an error we were returning HttpStatus.OK instead of HttpStatus.INTERNAL_SERVER_ERROR
16) Return statement of getAvailableBooks in RouteContoller.java try block returned mockApiService.getBooks() instead of availableBooks.
