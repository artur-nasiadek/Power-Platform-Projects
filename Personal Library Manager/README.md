## Personal Library Manager w/ Power Apps, Power Automate, Dataverse, Google Books API

<h4>This app helps to keep track of books in user's personal library.
The user can add a book into the app by scanning the book's barcode that contains ISBN. Using Google Books API the app extracts for the given ISBN the book's details:
<p></p>
<ul>
<li>title,</li>
<li>author's name,</li>
<li>book cover image.</li>
</ul>
<p></p>
The details are added into Dataverse table that feeds the app.</h4>
<br>

<h3>Walkthrough of the app</h3>

After opening the app the *welcome screen* is displayed with app's name and a button that leads to the list of books that have been already added to the app.
<p></p>
<p><b>Welcome screen</b></p>
<img src="/Personal%20Library%20Manager/Images/WelcomeScreen.jpg" width="200">

On the next screen the list of books is displayed. The list can be filtered with the *search book* field by title and author's name, and also with buttons: *read* and *unread*. Additionally, the list can be sorted by title, author's name or book rating. In order to add new book into the books collection the user has to press the *add new book* button, which will open the barcode scanner. After scanning the new book's ISBN barcode, a Power Automate flow is activated. In the flow the ISBN is used to extract the book's details from Google Books. The extracted information is populated in the Dataverse table and the new book is displayed on the list of books. 

<p><b>Books list screen</b></p>
<img src="/Personal%20Library%20Manager/Images/BooksListScreen.jpg" width="200">

By pressing on any item on the list a new screen is dispalyed containing the selected book's details and date of adding into the app. Additionally, there are options for the user to edit: status *read*/*unread* and rating. Pressing the *back to my bookcase* button will take the user back to the list of books.

<p><b>Book info screen</b></p>
<img src="/Personal%20Library%20Manager/Images/BookInfoScreen.jpg" width="200">

