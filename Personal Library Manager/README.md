## Personal Library Manager w/ Power Apps, Power Automate, Dataverse

This app helps to keep track of books in user's personal library.
The user can add a book into the app by scanning the book's barcode that contains ISBN. Using Google Books API the app extracts for the given ISBN the book's details:
- title,
- author's name,
- book cover image.

The details are added into Dataverse table that feeds the app.


Welcome screen

<img src="/Personal%20Library%20Manager/Images/WelcomeScreen.jpg" width="200"> After opening the app the welcome screen is displayed with app's name and a buttom that leads to the list of books. 