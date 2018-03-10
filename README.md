# Project 5
Restaurant App Menu application - CRUD, third party login providers

# Navigating the Restaurant Menu Application
## Purpose
The application allows any public user to see a list of restaurants and menu items available in the restaurant menu application. 

## View restaurants and menu items (CRUD: Read)
Website reads restaurant and menu_item information from a SQLite database named restaurantmenuwithusers.db. This does not require that user be logged in.

## Add, edit, delete new restaurant and menu items (CRUD: Create, Update, Delete)
Website includes a form allowing users to add new restaurants and menu items - detailing name, description, price, course type and upon succesful saving, the record is tagged with creator's user id. Only logged in users can add records to the database, and only the creator is allowed edit and delete privileges.

## Authentication & Authorization
Create, delete and update operations requires authorization status prior to execution.  Public users are directed a restaurant listing page and menu items page that allows read, but no CRUD operations.

Page implements a third-party authentication & authorization service using Google Accounts instead of implementing a local authentication & authorization spec.

There is a 'Login' and 'Logout' button/link in the project. 

## API Endpoint
Navigate to http://localhost:5000/restaurant/JSON  or from http://localhost:5000/restaurant page click on 'Restaurants JSON' menu to view a JSON endpoint that serves the same information as displayed in the HTML endpoints for an arbitrary item in the catalog.

# Installations
## Fetch the Source Code and VM Configuration

**Windows:** Use the Git Bash program (installed with Git) to get a Unix-style terminal.
**Other systems:** Use your favorite terminal program.

From the terminal, run:

    git clone https://github.com/sherinkuruvilla/OAuth2.0 oauth

This will give you a directory named **oauth** complete with the source code for the flask application, a vagrantfile, and a bootstrap.sh file for installing all of the necessary tools.

## Run the virtual machine!

Using the terminal, change directory to oauth (**cd oauth**), then type **vagrant up** to launch your virtual machine.


## Running the Restaurant Menu App
Once it is up and running, type **vagrant ssh**. This will log your terminal into the virtual machine, and you'll get a Linux shell prompt. When you want to log out, type **exit** at the shell prompt.  To turn the virtual machine off (without deleting anything), type **vagrant halt**. If you do this, you'll need to run **vagrant up** again before you can log into it.


Now that you have Vagrant up and running type **vagrant ssh** to log into your VM.  change to the /vagrant directory by typing **cd /vagrant**. This will take you to the shared folder between your virtual machine and host machine.

Type **ls** to ensure that you are inside the directory that contains project.py, database_setup.py, and two directories named 'templates' and 'static'

Now type **python database_setup.py** to initialize the database.

Type **python lotsofmenus.py** to populate the database with restaurants and menu items. (Optional)

Type **python project.py** to run the Flask web server. In your browser visit **http://localhost:5000** to view the restaurant menu app.  You should be able to view, add, edit, and delete menu items and restaurants.



