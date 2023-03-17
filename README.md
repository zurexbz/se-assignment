# se-assignment

| **ID CAMP** | **Nama** | 
| ----------- | -------- |
| FE4487715 | Mohammad Firman Fardiansyah |

## Flowchart
![Mohammad Firman Fardiansyah_FE4487715](https://user-images.githubusercontent.com/83849481/225844444-042d8d2b-98bb-4deb-b182-ca86512fe14c.jpg)

## Pseudocode
```
PROGRAM LibaryApp

// Login/Registration Functionality
IF (user is not logged in) {
    DISPLAY login/registration page
    IF (user selects "register") {
	  READ AND WRITE "Nama" with string
	  READ AND WRITE "Email" with string
	  READ AND WRITE "Nomor Telepon" with string
	  READ AND WRITE "Password" with string
	  VERIFY email by user
        CREATE new user account
	  log in success
    } ELSE {
	  READ AND WRITE "Email" with string
	  READ AND WRITE "Password" with string
        VERIFY user information and log in
	  IF (invalid log in) {
	  	TRY again
		RESET password
		VERIFY email for reset password
        } ELSE {
		 log in success
	  }
    }
}

// Search Functionality
IF (user is logged in) {
    DISPLAY dashboard
    READ AND WRITE "Searching" to QUERY search book
    SEARCH DATABASE for books matching query
    IF (user search by author){
	 DISPLAY LIST search by author to user
	 IF (user click a book)
		DISPLAY details contents of the book
    } ELSE {
	 DISPLAY LIST search by tittle to user
	 IF (user click a book)
		DISPLAY details contents of the book
    }
}

// Borrowing Functionality
IF (user selects a book to borrow) {
    CHECK IF book is available
    IF (book is available) {
        STORE "name_of_book" to cart with default quantity 1 and long borrowed 1 day
	  UPDATE cart with user input quantity of books and long borrowed
	  CHECKOUT borrowed books
        DISPLAY confirmation massage to user
        UPDATE books availability quantity status //by system
    } ELSE {
        DISPLAY notification to user
	  MOVE to searching books page
    }
}

// Renewing Functionality
IF (user want to extend borrowing book) {
    CHECK IF book is eligible for renewal
    IF (book is eligible) {
        CHECKOUT borrowed books
        DISPLAY confirmation message to user
	  UPDATE books availability quantity status //by system
    } ELSE {
        DISPLAY error message to user
	  USER must to return the book before the due
    }
}

// Returning Functionality
IF (user selects a book to return) {
    REMOVE book from user's borrowed books list
    UPDATE book's availability status //by system
    DISPLAY history borrowing books from the user
}

END PROGRAM
```
