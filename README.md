# Book API

## Requirement, Analysis

Client send getBook(int bookId)to get book satisfy id = bookId.
Client send insertBook(Book book) to add a book.
## Design

### Server
- class Book extends Serializable
- interface BookShelfInterface
    * Book getBook(int bookId)
    * void insertBook(Book book)
- class BookShelf implement BookShelfInterface
- class Server

### Client
- interface BookShelfInterface
- class Client

### Enviroment
- gRPC
- Python 3


