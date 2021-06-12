# GoGettingStarted2021

This project was based on the training I completed from the [Pluralsight Go: Getting Started Course](https://app.pluralsight.com/library/courses/getting-started-with-go/table-of-contents)

#To Interatct with the API:
* Build the application and launch it using the following command **go build main.go**
* Start the executable on your local machine.
* The API is accessible at http://localhost:3000/users
* This application supports the following parameters when interacting with the API
  * **ID** //The ID field is used for GET, PUT and DELETE, if the post contains an ID it will fail.
  * **FirstName** - String
  * **LastName** - String
  * **PhoneNumber** - String
  * **ZipCode** - String
* Data is not persisted once the applicaiton is shutdown, this is not associated with a backend database

* Postman is a great applicaiton for interacting with the WEB API.

**Get**

A Get to http://localhost:3000/users will return all users that have been added to the struct
A Get to http://localhost:3000/users/1 will return the first user
A Get to http://localhost:3000/users/2 will return the second user and so on.

**Post**
{
  "FirstName":"[Firstname]


