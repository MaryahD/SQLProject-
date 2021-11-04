# SQLProject-
// Run a query that creates a table named Authors that has the following columns: AuthorID, FullName, BirthCountry. 

CREATE TABLE Authors ( 
 AuthorID INT PRIMARY KEY AUTO_INCREMENT,
 FullName VARCGAR(50) NOT NULL, 
 BirthCountry VARCHAR (50) NOT NULL );
 
// Run a query that creates a table named Books that has the following columns: BookID, Name, AuthorID.

CREATE TABLE Books (
  BookID int primary key auto_increment,
  Name VARCHAR (50) NOT NULL,
  AuthorID int,
  FOREGIN KEY (AuthorID ) references Authors(AuthorID) );
//   
 intsert into Books (name, AuthorID)
 vaules 
 ("Pride and Prejudice", 1), 
 ("Sense and Sensibility", 1), 
 ("The Pickwick Papers", 2) ; 
  
