# quiz-fever-app.github.io
# Quiz Fever
System for creating, managing and adding quizzes with free access

## Functionality
* User Registration
* Option for viewing and solving quizzes from other users
* Various categories
* Option for filtering quizzes by topic or search by title
* Keeping statistic for every user and every quiz
* Interactive test editor
* Fluid UX

## Technologies
* HTML, CSS, Javascript
* Lit-html, Page
* Github Pages, Back4App

## Views (Pages)
* **Welcome screen** - landing page
* **Login/Register** - regsitration with email, username and password
* **Profile Page** - information about created and completed tests
* **Quiz Browser** - list with tests and option to search by title or filter by category
* **Quiz Details** - additional description, test statistics, information about the author, and option to start a test
* **Quiz Contest Mode** - answering questions, each one with a separate view, option for skipping questions, as well as restarting the question
* **Quiz Results** - summary of the results with an option for previewing the wrong answers
* **Quiz Editor** - integrated editor for tests, questions and answers

## Implementaion
### Data Structure
### Collections
* Sessions (default)
* Users (default)
```javascript
{
    email: String,
    username: String, 
    password: String
}
```

* Quizzes
```javascript
{
    title: String,
    topic: String, 
    questionCount: Number
}
```

* Questions
```javascript
{
    text: String,
    answers: Array<String>,
    correctIndex: Number,
    quiz: Pointer<Quiz> 
}
```
* Solutions
```javascript
{
    quiz: Pointer<Quiz>,
    correct: Number
}
```

#### Access Control
* Guests can register, view the catalog, tests details and users profile pages
*  Registered users can do all the above, as well as view the tests, their test results, create and edit tests
* Only the creator of a test can edit and delete it
* Every registered user can solve someone else's tests
