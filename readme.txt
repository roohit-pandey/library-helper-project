Library Management System
Features:
---------
- Add books to the library collection
- Register new users with unique IDs
- Search for books by title (case-insensitive)
- View all books with detailed information (ID, title, author, available quantity)
- Users can borrow books if available
- Users can return borrowed books
- View list of books borrowed by a user
- Interactive console menu-driven interface for ease of use

Classes and Responsibilities:
-----------------------------
1. Book:
   - Attributes: book_id, title, author, quantity (available stock)
   - Methods: 
   - display_book_info(): Prints book details
   - check_availability(): Returns True if quantity > 0
   - update_quantity(quantity): Adjusts the quantity by the passed value

2. User:
   - Attributes: user_id, name, borrowed_books (list)
   - Methods:
   - borrow_book(book): Borrows a book if available and updates quantity
   - return_book(book): Returns a book and updates quantity
   - view_borrowed_books(): Shows books currently borrowed by the user

3. Library:
   - Maintains lists of Book objects and User objects
   - Methods to add books, register users, search books, list all books, and handle interactive inputs
   - Checks to avoid duplicate user IDs and book IDs when adding

How to Use:
-----------
- Run the script.
- Use the menu to perform operations by entering corresponding numbers.
- When adding users or books, provide the required details prompted by the system.
- Borrow or return books by entering user ID and book ID.
- Exit the program by selecting option 8.

Notes:
------
- User IDs and Book IDs must be unique.
- Book quantities are automatically updated when borrowing or returning.
- Searching books by title supports partial and case-insensitive matching.
- The program handles erroneous inputs like invalid IDs gracefully by notifying the user.