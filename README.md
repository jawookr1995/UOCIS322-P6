# UOCIS322-P6
UOCIS322 - Project 6 - REST API

## Author : Theodore Yun

## This web service app contains three services, brevetsapp, api, and website.

### How brevetsapp work
- It is ACP calculator page.

- It has two buttons which are submit and dislay.

- After you filling out the value in the chart, if you hit the "submit" button, your database will be stored into MongoDB database.

- If no value is inserted in ACP calculator page, "submit" button would cause error.

- After data is passed, if you hit "display" the database will be displayed in separate page.

### How to approach to application

- http://<host:port>/

- If you put your host machine in our case, testium would be fit for hostname, and assigned port should be included.

- In "docker-compose.yml" you can find applicable port number.


### How api works

* This is a Restful service that includes the following functionalities:

* Three basic APIs that exposes what is stored in MongoDB.three basic APIs:

  * "http://host:port/listAll" should return all open and close times in the database
  * "http://host:port/listOpenOnly" should return open times only
  * "http://host:port/listCloseOnly" should return close times only
* Two different representations: one in csv and one in json. For the above, JSON is the default representation for the above three basic APIs.

  * "http://host:port/listAll/csv" should return all open and close times in CSV format

  * "http://host:port/listOpenOnly/csv" should return open times only in CSV format

  * "http://host:port/listCloseOnly/csv" should return close times only in CSV format

  * "http://host:port/listAll/json" should return all open and close times in JSON format

  * http://host:port/listOpenOnly/json" should return open times only in JSON format

  * "http://host:port/listCloseOnly/json" should return close times only in JSON format

* A query parameter getting top "k" open and close times. For examples, see below.

  * "http://host:port/listOpenOnly/csv?top=3" should return top 3 open times only (in ascending order) in CSV format
  * "http://host:port/listOpenOnly/json?top=5" should return top 5 open times only (in ascending order) in JSON format
  * "http://host:port/listCloseOnly/csv?top=6" should return top 5 close times only (in ascending order) in CSV format
  * "http://host:port/listCloseOnly/json?top=4" should return top 4 close times only (in ascending order) in JSON format
  
- If you go to designated port for api, you will see all the types of listing. (Check detail in "docker-compose.yml")


## What is website

- You'll also design consumer programs to use the service that you expose. In my case, I used php.

- Testing process would be same. //http:<host:port>

# Credits

- Michal Young, Ram Durairajan, Steven Walton, Joe Istas.

