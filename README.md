0x00. AirBnB clone - The console
This project is collaborated by Sufian Hamza and Gideon Gyebi as part of our ALX-SE program.

This represents a streamlined imitation of the Airbnb service, constructed as a command-line program. 
The console will be able to perform tasks lik:
1. create a new object
2. retrive an object from a file
3. do operations on objects
4. destroy an object
5. Storage

Acting as the user's point of contact with the application, the command interpreter facilitates engagement and execution of diverse commands.

installation
git clone https://github.com/zee-ham-su/AirBnB_clone.git

cd into the AirBnb directory and then run the command
./console.py

The console should work in both interactive and non interactive modes as demonstrated below:

Execution
Your shell should work like this in interactive mode:

$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb)
(hbnb) 
(hbnb) quit
$

But also in non-interactive mode: 

$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$

Testing:
all the test models can be find in th tests directory and adhered to the Python unittest module

Test should also run in both interactive and non interactive modes
, for example:

Unit tests must also pass in non-interactive mode:

guillaume@ubuntu:~/AirBnB$ echo "python3 -m unittest discover tests" | bash
...................................................................................
...................................................................................
.......................
----------------------------------------------------------------------
Ran 189 tests in 13.135s

OK

Unit tests in interactiv mode:
All your files, classes, functions must be tested with unit tests

guillaume@ubuntu:~/AirBnB$ python3 -m unittest discover tests
...................................................................................
...................................................................................
.......................
----------------------------------------------------------------------
Ran 189 tests in 13.135s

OK
guillaume@ubuntu:~/AirBnB$

Documentation
All your modules should have a documentation (python3 -c 'print(__import__("my_module").__doc__)')
All your classes should have a documentation (python3 -c 'print(__import__("my_module").MyClass.__doc__)')
All your functions (inside and outside a class) should have a documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)')
A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)

Commands Usage

create
create <class>

(hbnb) create BaseModel
38a22b25-ae9c-4fa9-9f94-59b3eb51bfba
(hbnb)

show
show <class> <id>
(hbnb) User.show("246c227a-d5c1-403d-9bc7-6a47bb9f0f68")
[User] (246c227a-d5c1-403d-9bc7-6a47bb9f0f68) {'first_name': 'Betty', 'last_name': 'Bar', 'created_at': datetime.datetime(2017, 9, 28, 21, 12, 19, 611352), 'updated_at': datetime.datetime(2017, 9, 28, 21, 12, 19, 611363), 'password': '63a9f0ea7bb98050796b649e85481845', 'email': 'airbnb@mail.com', 'id': '246c227a-d5c1-403d-9bc7-6a47bb9f0f68'}
(hbnb)

all
(hbnb) create BaseModel
e45ddda9-eb80-4858-99a9-226d4f08a629
(hbnb) all BaseModel
["[BaseModel] (4c8f7ebc-257f-4ed1-b26b-e7aace459897) [BaseModel] (4c8f7ebc-257f-4ed1-b26b-e7aace459897) {'id': '4c8f7ebc-257f-4ed1-b26b-e7aace459897', 'created_at': datetime.datetime(2021, 11, 13, 22, 19, 19, 447155), 'updated_at': datetime.datetime(2021, 11, 13, 22, 19, 19, 447257), 'name': 'My First Model', 'my_number': 89}"]
["[BaseModel]

destroy
(hbnb) User.count()
2
(hbnb) User.destroy("246c227a-d5c1-403d-9bc7-6a47bb9f0f68")
(hbnb) User.count()
1
(hbnb)

count
(hbnb) User.count()
2
(hbnb) 

update

(hbnb) User.show("38f22813-2753-4d42-b37c-57a17f1e4f88")
[User] (38f22813-2753-4d42-b37c-57a17f1e4f88) {'first_name': 'Betty', 'last_name': 'Bar', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848279), 'updated_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848291), 'password': 'b9be11166d72e9e3ae7fd407165e4bd2', 'email': 'airbnb@mail.com', 'id': '38f22813-2753-4d42-b37c-57a17f1e4f88'}
(hbnb)
(hbnb) User.update("38f22813-2753-4d42-b37c-57a17f1e4f88", "first_name", "John")
(hbnb) User.update("38f22813-2753-4d42-b37c-57a17f1e4f88", "age", 89)
(hbnb)
(hbnb) User.show("38f22813-2753-4d42-b37c-57a17f1e4f88")
[User] (38f22813-2753-4d42-b37c-57a17f1e4f88) {'age': 89, 'first_name': 'John', 'last_name': 'Bar', 'created_at': datetime.datetime(2017, 9, 28, 21, 11, 42, 848279), 'updated_at': datetime.datetime(2017, 9, 28, 21, 15, 32, 299055), 'password': 'b9be11166d72e9e3ae7fd407165e4bd2', 'email': 'airbnb@mail.com', 'id': '38f22813-2753-4d42-b37c-57a17f1e4f88'}
(hbnb) 






