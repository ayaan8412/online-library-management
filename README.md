<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Online Library Management System</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css">
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">Online Library</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#home">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#books">Books</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#about">About</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <header id="home" class="bg-dark text-light p-5 text-center">
        <h1 class="display-4">Welcome to our Online Library</h1>
        <p class="lead">Discover new books, authors, and genres</p>
    </header>
    <section id="featured" class="p-5 bg-light">
        <h2 class="mb-4">Featured Books</h2>
        <div class="row row-cols-1 row-cols-md-3 g-4">
            <div class="col">
                <div class="card">
                    <img src="https://picsum.photos/200/300" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">spanning tree</h5>
                        <p class="card-text">spanning Three continents and eight generations</p>
                        <p>Author: Yaa Gyasi,2016</p>
                        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#bookModal">View Details</button>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="https://picsum.photos/200/301" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">Home Going</h5>
                        <p class="card-text">a story about a mother and a son </p>
                        <p>Author: Jane Doe</p>
                        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#bookModal">View Details</button>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="https://picsum.photos/200/302" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">The Great Gatsby </h5>
                        <p class="card-text">f.scott</p>
                        <p>Author: Bob Smith</p>
                        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#bookModal">View Details</button>
                    </div>
                </div>
            </div>
        </div>
        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#addBookModal">Add New Book</button>
        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#addAuthorModal">Add New Author</button>
    </section>
    <section id="books" class="p-5 bg-light">
        <h2 class="mb-4">All Books</h2>
        <input type="text" id="search" class="form-control" placeholder="Search for books">
        <table class="table table-striped table-hover">
            <thead>
                <tr>
                    <th scope="col">Title</th>
                    <th scope="col">Author</th>
                    <th scope="col">Genre</th>
                </tr>
            </thead>
            <tbody id="bookTable">
                <tr>
                    <td>Book Title</td>
                    <td>John Doe</td>
                    <td>Fiction</td>
                </tr>
                <tr>
                    <td>Book Title</td>
                    <td>Jane Doe</td>
                    <td>Non-Fiction</td>
                </tr>
                <tr>
                    <td>Book Title</td>
                    <td>Bob Smith</td>
                    <td>Fantasy</td>
                </tr>
            </tbody>
        </table>
    </section>
    <section id="about" class="p-5 bg-light">
        <h2 class="mb-4">About Us</h2>
        <p>The narative often delves into the complexities of love family,and the challenges.</p>
    </section>
    <div class="modal fade" id="bookModal" tabindex="-1" aria-labelledby="bookModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="bookModalLabel">Book Details</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <h5>Book Title</h5>
                    <p>Book Description</p>
                    <p>Author: John Doe</p>
                    <p>Genre: Fiction</p>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="addBookModal" tabindex="-1" aria-labelledby="addBookModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="addBookModalLabel">Add New Book</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="addBookForm">
                        <div class="mb-3">
                            <label for="bookTitle" class="form-label">Book Title</label>
                            <input type="text" class="form-control" id="bookTitle" required>
                        </div>
                        <div class="mb-3">
                            <label for="bookAuthor" class="form-label">Author</label>
                            <input type="text" class="form-control" id="bookAuthor" required>
                        </div>
                        <div class="mb-3">
                            <label for="bookGenre" class="form-label">Genre</label>
                            <input type="text" class="form-control" id="bookGenre" required>
                        </div>
                        <div class="mb-3">
                            <label for="bookDescription" class="form-label">Description</label>
                            <textarea class="form-control" id="bookDescription" required></textarea>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                    <button type="button" class="btn btn-primary" id="addBookBtn">Add Book</button>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="addAuthorModal" tabindex="-1" aria-labelledby="addAuthorModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="addAuthorModalLabel">Add New Author</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="addAuthorForm">
                        <div class="mb-3">
                            <label for="authorName" class="form-label">Author Name</label>
                            <input type="text" class="form-control" id="authorName" required>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                    <button type="button" class="btn btn-primary" id="addAuthorBtn">Add Author</button>
                </div>
            </div>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        const searchInput = document.getElementById('search');
        const bookTable = document.getElementById('bookTable');
        const addBookForm = document.getElementById('addBookForm');
        const addAuthorForm = document.getElementById('addAuthorForm');
        const addBookBtn = document.getElementById('addBookBtn');
        const addAuthorBtn = document.getElementById('addAuthorBtn');

        searchInput.addEventListener('input', (e) => {
            const searchTerm = e.target.value.toLowerCase();
            const rows = bookTable.rows;

            for (let i = 0; i < rows.length; i++) {
                const row = rows[i];
                const title = row.cells[0].textContent.toLowerCase();
                const author = row.cells[1].textContent.toLowerCase();
                const genre = row.cells[2].textContent.toLowerCase();

                if (title.includes(searchTerm) || author.includes(searchTerm) || genre.includes(searchTerm)) {
                    row.style.display = '';
                } else {
                    row.style.display = 'none';
                }
            }
        });

        addBookBtn.addEventListener('click', () => {
            const bookTitle = document.getElementById('bookTitle').value;
            const bookAuthor = document.getElementById('bookAuthor').value;
            const bookGenre = document.getElementById('bookGenre').value;
            const bookDescription = document.getElementById('bookDescription').value;

            const newBook = { title: bookTitle, author: bookAuthor, genre: bookGenre, description: bookDescription };
            books.push(newBook);

            const newRow = document.createElement('tr');
            const titleCell = document.createElement('td');
            const authorCell = document.createElement('td');
            const genreCell = document.createElement('td');

            titleCell.textContent = bookTitle;
            authorCell.textContent = bookAuthor;
            genreCell.textContent = bookGenre;

            newRow.appendChild(titleCell);
            newRow.appendChild(authorCell);
            newRow.appendChild(genreCell);

            bookTable.appendChild(newRow);

            addBookForm.reset();
        });

        addAuthorBtn.addEventListener('click', () => {
            const authorName = document.getElementById('authorName').value;

            const newAuthor = { name: authorName };
            authors.push(newAuthor);

            addAuthorForm.reset();
        });

        window.onload = () => {
            for (let i = 0; i < books.length; i++) {
                const book = books[i];

                const row = document.createElement('tr');
                const titleCell = document.createElement('td');
                const authorCell = document.createElement('td');
                const genreCell = document.createElement('td');

                titleCell.textContent = book.title;
                authorCell.textContent = book.author;
                genreCell.textContent = book.genre;

                row.appendChild(titleCell);
                row.appendChild(authorCell);
                row.appendChild(genreCell);

                bookTable.appendChild(row);
            }
        };
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Online Library Management System</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css">
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">Online Library</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#home">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#books">Books</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#about">About</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <header id="home" class="bg-dark text-light p-5 text-center">
        <h1 class="display-4">Welcome to our Online Library</h1>
        <p class="lead">Discover new books, authors, and genres</p>
    </header>
    <section id="featured" class="p-5 bg-light">
        <h2 class="mb-4">Featured Books</h2>
        <div class="row row-cols-1 row-cols-md-3 g-4">
            <div class="col">
                <div class="card">
                    <img src="https://picsum.photos/200/300" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">spanning tree</h5>
                        <p class="card-text">spanning Three continents and eight generations</p>
                        <p>Author: Yaa Gyasi,2016</p>
                        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#bookModal">View Details</button>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="https://picsum.photos/200/301" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">Home Going</h5>
                        <p class="card-text">a story about a mother and a son </p>
                        <p>Author: Jane Doe</p>
                        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#bookModal">View Details</button>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="https://picsum.photos/200/302" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">The Great Gatsby </h5>
                        <p class="card-text">f.scott</p>
                        <p>Author: Bob Smith</p>
                        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#bookModal">View Details</button>
                    </div>
                </div>
            </div>
        </div>
        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#addBookModal">Add New Book</button>
        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#addAuthorModal">Add New Author</button>
    </section>
    <section id="books" class="p-5 bg-light">
        <h2 class="mb-4">All Books</h2>
        <input type="text" id="search" class="form-control" placeholder="Search for books">
        <table class="table table-striped table-hover">
            <thead>
                <tr>
                    <th scope="col">Title</th>
                    <th scope="col">Author</th>
                    <th scope="col">Genre</th>
                </tr>
            </thead>
            <tbody id="bookTable">
                <tr>
                    <td>Book Title</td>
                    <td>John Doe</td>
                    <td>Fiction</td>
                </tr>
                <tr>
                    <td>Book Title</td>
                    <td>Jane Doe</td>
                    <td>Non-Fiction</td>
                </tr>
                <tr>
                    <td>Book Title</td>
                    <td>Bob Smith</td>
                    <td>Fantasy</td>
                </tr>
            </tbody>
        </table>
    </section>
    <section id="about" class="p-5 bg-light">
        <h2 class="mb-4">About Us</h2>
        <p>The narative often delves into the complexities of love family,and the challenges.</p>
    </section>
    <div class="modal fade" id="bookModal" tabindex="-1" aria-labelledby="bookModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="bookModalLabel">Book Details</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <h5>Book Title</h5>
                    <p>Book Description</p>
                    <p>Author: John Doe</p>
                    <p>Genre: Fiction</p>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="addBookModal" tabindex="-1" aria-labelledby="addBookModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="addBookModalLabel">Add New Book</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="addBookForm">
                        <div class="mb-3">
                            <label for="bookTitle" class="form-label">Book Title</label>
                            <input type="text" class="form-control" id="bookTitle" required>
                        </div>
                        <div class="mb-3">
                            <label for="bookAuthor" class="form-label">Author</label>
                            <input type="text" class="form-control" id="bookAuthor" required>
                        </div>
                        <div class="mb-3">
                            <label for="bookGenre" class="form-label">Genre</label>
                            <input type="text" class="form-control" id="bookGenre" required>
                        </div>
                        <div class="mb-3">
                            <label for="bookDescription" class="form-label">Description</label>
                            <textarea class="form-control" id="bookDescription" required></textarea>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                    <button type="button" class="btn btn-primary" id="addBookBtn">Add Book</button>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="addAuthorModal" tabindex="-1" aria-labelledby="addAuthorModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="addAuthorModalLabel">Add New Author</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="addAuthorForm">
                        <div class="mb-3">
                            <label for="authorName" class="form-label">Author Name</label>
                            <input type="text" class="form-control" id="authorName" required>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                    <button type="button" class="btn btn-primary" id="addAuthorBtn">Add Author</button>
                </div>
            </div>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        const searchInput = document.getElementById('search');
        const bookTable = document.getElementById('bookTable');
        const addBookForm = document.getElementById('addBookForm');
        const addAuthorForm = document.getElementById('addAuthorForm');
        const addBookBtn = document.getElementById('addBookBtn');
        const addAuthorBtn = document.getElementById('addAuthorBtn');

        searchInput.addEventListener('input', (e) => {
            const searchTerm = e.target.value.toLowerCase();
            const rows = bookTable.rows;

            for (let i = 0; i < rows.length; i++) {
                const row = rows[i];
                const title = row.cells[0].textContent.toLowerCase();
                const author = row.cells[1].textContent.toLowerCase();
                const genre = row.cells[2].textContent.toLowerCase();

                if (title.includes(searchTerm) || author.includes(searchTerm) || genre.includes(searchTerm)) {
                    row.style.display = '';
                } else {
                    row.style.display = 'none';
                }
            }
        });

        addBookBtn.addEventListener('click', () => {
            const bookTitle = document.getElementById('bookTitle').value;
            const bookAuthor = document.getElementById('bookAuthor').value;
            const bookGenre = document.getElementById('bookGenre').value;
            const bookDescription = document.getElementById('bookDescription').value;

            const newBook = { title: bookTitle, author: bookAuthor, genre: bookGenre, description: bookDescription };
            books.push(newBook);

            const newRow = document.createElement('tr');
            const titleCell = document.createElement('td');
            const authorCell = document.createElement('td');
            const genreCell = document.createElement('td');

            titleCell.textContent = bookTitle;
            authorCell.textContent = bookAuthor;
            genreCell.textContent = bookGenre;

            newRow.appendChild(titleCell);
            newRow.appendChild(authorCell);
            newRow.appendChild(genreCell);

            bookTable.appendChild(newRow);

            addBookForm.reset();
        });

        addAuthorBtn.addEventListener('click', () => {
            const authorName = document.getElementById('authorName').value;

            const newAuthor = { name: authorName };
            authors.push(newAuthor);

            addAuthorForm.reset();
        });

        window.onload = () => {
            for (let i = 0; i < books.length; i++) {
                const book = books[i];

                const row = document.createElement('tr');
                const titleCell = document.createElement('td');
                const authorCell = document.createElement('td');
                const genreCell = document.createElement('td');

                titleCell.textContent = book.title;
                authorCell.textContent = book.author;
                genreCell.textContent = book.genre;

                row.appendChild(titleCell);
                row.appendChild(authorCell);
                row.appendChild(genreCell);

                bookTable.appendChild(row);
            }
        };
    </script>
</body>
</html>
