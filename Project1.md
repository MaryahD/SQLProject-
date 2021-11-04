# SQLProject-

> Run a query that creates a table named Authors that has the following columns: AuthorID, FullName, BirthCountry. 
```ruby
CREATE TABLE Authors ( 
 AuthorID INT PRIMARY KEY AUTO_INCREMENT,
 FullName VARCGAR(50) NOT NULL, 
 BirthCountry VARCHAR (50) NOT NULL );
 ```
 > Run a query that creates a table named Books that has the following columns: BookID, Name, AuthorID.
```ruby
CREATE TABLE Books (
  BookID int primary key auto_increment,
  Name VARCHAR (50) NOT NULL,
  AuthorID int,
  FOREGIN KEY (AuthorID ) references Authors(AuthorID) );
```  
> Add the following the Books table:
```ruby
 intsert into Books (name, AuthorID)
 vaules 
 ("Pride and Prejudice", 1), 
 ("Sense and Sensibility", 1), 
 ("The Pickwick Papers", 2) ; 
 ``` 
 > Run a query that joins the Authors and Books table together using the AuthorID foreign key.
```ruby
select * from Books
join Authors 
using (authorID); 
```
> Next, create a view named AuthorBooks using the join query created in step 1 adding the following parameters: Show only the Authors full name and book name. Rename the column name results using the AS keyword. The Authors FullName should display as AuthorName.
The Books Name should display as BookName. Order the results alphabetically by the authors full name.
```ruby
Create view AuthorBooks as 
select  full name as AuthorsName, name as BookName
From authors
inner join Books
on Authors.authorID = Books.auhtorID 
order by  AuthorsName; 
```
