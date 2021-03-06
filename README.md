## How to use

 ### To set up the project:

 Clone this repository and then run bundle to install dependencies:

 ```
 git clone git@github.com:mbrad26/chitter-challenge.git

 bundle install
 ```

 ### To run the Chitter app:

 ```
 rackup
 ```

 To view Chitter app in action navigate to "localhost:9292/"

 ### To run tests:

 ```
 rspec
 ```

 ### To run linting:

 ```
 rubocop
 ```

## Setting up the databases

This app uses PostgreSQL to manage the databases:

```bash
brew install postgresql

brew services start postgresql

psql postgres

# list databases
\l
# quit psql
\q
```

## To set up the database

Connect to 'psql' and create 'chitter' database:

```
CREATE DATABASE chitter;
CREATE DATABASE chitter-test;
```

To set up the tables for the ```chitter``` database run the SQL scripts inside the "db/migrations" folder.

## Running tests


```bash
# Runs test suite
rspec
```

## Starting the app on the localhost

```bash
# Starts the server on port 9292
rackup

```

## Implementation

```
As a Maker
So that I can let people know what I am doing  
I want to post a message (peep) to chitter
```
* write the feature test
* add text-area and form for creating and posting peeps to the index.erb
* create get and post routes
* make the test pass in the simplest way
* create and connect to database
* configured testing environment
* implemented class methods to facilitate the creation and retrieval of peeps from database

```
As a maker
So that I can see what others are saying  
I want to see all peeps in reverse chronological order
```
* write the feature test
* changed the query string in ```Peep.all``` to reflect the user story

```
As a Maker
So that I can better appreciate the context of a peep
I want to see the time at which it was made
```
* refactored unit tests and wrapped database data in Ruby objects
* write the feature test
* updated index.erb

```
As a Maker
So that I can post messages on Chitter as me
I want to sign up for Chitter
```
* write the feature test
* make the test pass by creating the controllers and '/users/new.erb'
* create the ```users``` table
* write unit test and implement ```User``` class method for the creation of users
* write unit test and implement password encryption

```
As a Maker
So that only I can post messages on Chitter as me
I want to log in to Chitter
```
* write the feature tests
* create the log in view and update the controller with the required paths
* write unit tests for authentication in User class

## To do

* to implement the last two user story
* to add some CSS
* to extract the database setup into an object
