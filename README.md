Introduction to the service:
Welcome to our vinyl website for music lovers! Here you'll find a great selection of vinyl records from various genres, ranging from classic rock to jazz and everything in between. We offer competitive prices and are always on the lookout for new and exciting titles to add to our collection.

In addition to our selection of vinyl records, we also offer a variety of features to enhance your shopping experience. You can rate and review records, add them to your wishlist, and even leave comments on individual record pages. We also have a helpful search function to help you find exactly what you're looking for.

We pride ourselves on providing top-notch customer service and want to ensure that your experience with us is always a positive one. So, whether you're a seasoned vinyl collector or just getting started, we hope you'll find something you love on our website. Happy shopping!

Team members description, contributions of each team member:

Myrzabekov Farkhat:
Created the database and implemented the struct Record to store all main info about vinyl recordings, Worked on rendering (passing) the data to templates
Added two new fields to the records database (sale and preorder)
Worked on website design by adding a 3D model iframe
Implemented registration and login/logout functionality for users
Added sessions table to db to keep logged users in their accounts using the "github.com/gorilla/sessions" library
Created a template to display a user's wishlist using a table
Added an HTML page for adding a new vinyl record to a database
Parsed form data for the new record's title, artist, genre, and price, and also retrieved the image file


Nashkenova Ingkar:
Designed project structure, especially how to represent vinyls list

Implemented sorting system based on different fields such as price and author

Added functionality to search vinyls by keywords

Redesigned searching and filtering using two forms on a web page

Created a go handler to apply filters and search to display data based on queries

Processed the uploaded image for a new added record by creating a unique filename and saving the image file to the server

Added a function to insert a new wishlist item into the database using the user's ID and the record ID obtained from the request form data

Completed the rating system, allowing users to rate vinyl records and displaying the ratings in the UI


Explanation how to run the code:
open command line in project folder and type "go run main.go", then go to page http://localhost:8080/

Explanation of each feature with screen of code and the output result:
![image](https://user-images.githubusercontent.com/91084290/226188179-a7365ec0-6cc9-4ffb-acc0-992bc89048fb.png)
Go HTTP handler function that handles user registration. It parses the form data submitted by the user, inserts the email and password into the users table of a SQLite database, and redirects the user to the home page.
![image](https://user-images.githubusercontent.com/91084290/226188345-e07fca6b-923a-4682-90f7-f6ce0b222fd0.png)
function that handles user logins. It parses the form data for user email and password, verifies the user's credentials, creates a session for the user, and sets a session cookie before redirecting the user to the homepage.
![image](https://user-images.githubusercontent.com/91084290/226188861-17a3aeff-c215-4fa8-bec2-13ba8ce671ff.png)


![image](https://user-images.githubusercontent.com/91084290/226188413-99a4be18-f0b6-4b39-9345-d0e5e08d94aa.png)
simply logout function clears seesion for logged in user
![image](https://user-images.githubusercontent.com/91084290/226188893-b36409ea-e181-4a4e-992b-0cb66421b994.png)

![image](https://user-images.githubusercontent.com/91084290/226188604-8d78b5bc-6b34-4c12-bafb-1cbc0d105ce9.png)
![image](https://user-images.githubusercontent.com/91084290/226188616-a4921a02-da07-4323-970e-9be38f895891.png)

This code defines a function to handle a request for all records. It connects to a SQLite database, queries for records with an optional sorting parameter, and displays the results in a template. It also allows for filtering of the results based on a search query and filter parameters for price and rating. It checks for a session cookie and displays the user's email if there is a corresponding user in the database.
![image](https://user-images.githubusercontent.com/91084290/226188913-b93b2bad-2639-4490-b095-89f2c56393e9.png)



![image](https://user-images.githubusercontent.com/91084290/226188707-298250ff-4519-405d-bea7-260a90338e57.png)
![image](https://user-images.githubusercontent.com/91084290/226188720-c31523b5-b000-42e4-914a-83f0446b3a79.png)

function that handles adding a new record to a database. It parses the HTTP request, extracts the record data and image file, saves the image to a public directory, creates a new record object, and adds it to the database. 
![image](https://user-images.githubusercontent.com/91084290/226188930-3624a632-99dc-462e-8364-96109d545236.png)



![image](https://user-images.githubusercontent.com/91084290/226188801-4afe37fd-4bf5-4425-a605-78dcb764ef57.png)
function that displays the wishlist of a logged-in user. It retrieves the user's ID from a session cookie, queries the database to retrieve the records in the wishlist, and displays them using a template.
![image](https://user-images.githubusercontent.com/91084290/226188950-34fea145-88f8-4d7a-83bb-70627cb2a5e7.png)

![image](https://user-images.githubusercontent.com/91084290/226189136-18bfbaf6-f0ac-4fcc-8ba0-94fe9d0d5fb6.png)
func to make adding ratings for vinyl records. It parses the form data for the record ID and the rating, updates the record's total rating and count in the database, calculates the new rating, and redirects the user back to the homepage.
![image](https://user-images.githubusercontent.com/91084290/226189186-627a58be-bda5-48e0-9915-82c34c69ff24.png)





