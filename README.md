# cit281-lab6
## Part 1: Join GitHub and work through Introduction to GitHub course
<img width="78" alt="Screenshot 2023-06-06 at 9 37 23 AM" src="https://github.com/mmathes2/cit281-lab6/assets/134009490/8df4e230-641f-4fb4-a4aa-bd38c97ad320">

## Part 2: Create lab file
<img width="216" alt="Screenshot 2023-06-06 at 9 38 11 AM" src="https://github.com/mmathes2/cit281-lab6/assets/134009490/1b36e9f2-7d6b-46a7-ad02-6c95ceee221e">

## Part 3: Classes overview
<img width="649" alt="Screenshot 2023-06-06 at 9 38 33 AM" src="https://github.com/mmathes2/cit281-lab6/assets/134009490/9eb05407-0c01-42f0-9206-19c1eb701854">

## Part 4: Create and test Book class
```
class Book {
  constructor(title, author, pubDate) {
    this.title = title;
    this.author = author;
    this.pubDate = pubDate;
  }
}
// Create a book
const atomicHabits = new Book("Atomic Habits", "James Clear", "10/16/2018");
```
## Part 5: Create and test Library class
```
class Library {
  constructor(name) {
    this._name = name;
    this._books = [];
  }
  
  get books() {
    // Return copy of books
    return JSON.parse(JSON.stringify(this._books));
  }
  
  get count() {
    return this._books.length;
  }
  
  addBook(book = {}) {
    const { title = "", author = "", pubDate = "" } = book;
    if (title.length > 0 && author.length > 0) {
      const newBook = { title, author, pubDate };
      this._books.push(newBook);
    }
  }
  
  listBooks() {
    for (const book of this._books) {
      const {title, author, pubDate, isbn} = book;
      console.log(`Title: ${title}, Author: ${author}, PubDate: ${pubDate}`)
    }
  }
}

// Create library object
const library = new Library("New York Times Best Seller List");

// Create a book
const atomicHabits = new Book("Atomic Habits", "James Clear", "10/16/2018");

// Add book to library and output library count and books
library.addBook(atomicHabits);
console.log(`Book count: ${library.count}`);
library.listBooks();
```
## Part 6: Add at least two more books to the library
<img width="571" alt="Screenshot 2023-06-06 at 9 42 19 AM" src="https://github.com/mmathes2/cit281-lab6/assets/134009490/c1dcc4bd-27fd-4ac8-9b1e-75c550474c77">

## Part 7: Add ISBN and a delete book method
<img width="299" alt="Screenshot 2023-06-06 at 9 43 05 AM" src="https://github.com/mmathes2/cit281-lab6/assets/134009490/0485dd40-64bf-4710-9ea3-08e0f2484456">
