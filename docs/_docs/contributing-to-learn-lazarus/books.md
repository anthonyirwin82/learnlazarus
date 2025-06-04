---
title: Adding books to Learn Lazarus
permalink: /docs/adding-to-learn-lazarus/books
order: 2
---
If there is a new book that you feel would be valuable for others to know about and you want to add it to learn lazarus then you need to follow the following guidelines:

* If the books is free then it needs to be able to be downloaded legally for free. (no pirate copies)
* If the book author allows people to freely redistibute the book then a copy should be added to the learn lazarus website to avoid any potential broken links in the future.
* If redistribution is not allowed then a link to the original source should be used instead.
* If the book has examples then the zip file or source code repository should be linked. (Again if the code is freely redistributable then a zip copy should be added to the learn lazarus website)

What information you will need:

* A book cover image (ideally sized appropriately not a huge fullscreen image)
* The book title
* The book author
* A short description of the book. {{"<p></p>" | escape }} tags can be used for multiple paragraph descriptions but the description should not exceed the height of the book image and download buttons.
* A download link for the book
* A download link for the book code examples
* A link to the book authors website. Linking to the book if they have a page for the book on their website.

Location for files:
* Book cover images at ```learnlazarus/docs/assets/img/books```
* Book pdf download at ```learnlazarus/docs/assets/downloads/books```
* Book code examples zip download at ```learnlazarus/docs/assets/downloads/books```

Below is an empty template you can copy and paste into the ```learnlazarus/docs/_docs/getting-started/books.md``` file.

```liquid
{% raw %}
{% include book.html 
   img="" 
   title="" 
   author=""
   author_website=""
   description=""
   book_btn=""
   examples_btn=""
%}
{% endraw %}
```

The fields should be obvious by name but you can check existing entries in the books.md file if you are unsure.

The urls for content on learn lazarus should be as follows:
* Book cover images ```/assets/img/books/image_filename.png```
* Book pdf files ```/assets/downloads/books/book_filename.pdf```
* Book code examples zip files ```/assets/downloads/books/code_examples_filename.zip```

If you don't have information to provide for one of the options then it should be removed. Do not leave empty fields as it will be processed by the liquid template engine. Removing the field will stop it being rendered to the website.

You should then build a local copy of the website and test your changes in your web browser to make sure it works correctly. Once you are happy with the changes you can make a pull request to have the changes reviewed and added to the learn lazarus website.