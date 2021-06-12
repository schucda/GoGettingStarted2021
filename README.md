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
Gets users from the struct

A Get to http://localhost:3000/users will return all users that have been added to the struct
A Get to http://localhost:3000/users/1 will return the first user
A Get to http://localhost:3000/users/2 will return the second user and so on.

**Post**
Adds users to the struct

{
  "FirstName":"[First name]",
  "LastName":"[last name]",
  "PhoneNumber":"[phone number]",
  "ZipCode":"[zip code]"
}

**Put**
Updates users in the struct

When doing this, you must **put** to the appropriate URL, for example, if I want to update the 3rd user, I must go to https://localhost:3000/users/3
The **put** must be structured as follows:

{
  "ID":[number]
  "FirstName":"[First name]",
  "LastName":"[last name]",
  "PhoneNumber":"[phone number]",
  "ZipCode":"[zip code]"
}

if a field is left blank or the ID doesn't match the URL path it will fail.

**Delete**
Delete a user from the application

Issue the delete to the appropriate URL https://localhost:3000/users/3

{
  "ID":3
}

This will delete the user at 3

#Future improvement will include:
* Adding a WEBUI, currently interact with this applicaiton through POSTMAN
* Associating with a backend database



