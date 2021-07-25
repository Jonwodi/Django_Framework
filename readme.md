
# DJANGO FRAMEWORK
Python has a great set of tools called Django for building web applications. Django is a web framework - a set of tools designed to build interactive websites.

URL for Django documentation = https://www.djangoproject.com/

# Setting Up a Project - Writing a Spec
A full spec (specification) details the project goals, describes the project's functionality, and discusses its appearance and user interface.

# Setting Up a Project - Creating/Activating a Virtual Environment
To have access to and be able to work with Django we first have to set up a virtual environment. A virtual environment is place on your system where you can install packages and isolate them from all other python packages.

Step 1: Create a new directory (folder) using the command (mkdir project_name) using a terminal e.g. windows powershell for window users. 

Step 2: Then use the command (cd) to enter that directory that you created. Then open that directory in a text editor (visual studio code) using the command (code .).

Step 3: Once the project folder is open in visual studio code, start a terminal and enter the command (pipenv shell), to create and activate a virtual environment for your project.

Note: to deactivate virtual environment simply close the terminal.

# Installing Django
After entering the command (pipenv shell) in your vs code terminal, a Pipfile should have been created for your project.

Copy and paste, the django package under packages and do the same for the development (dev) packages if your project needs them. Your Pipfile should look similar as shown below:

[dev-packages]

isort = "==5.2.1"

flake8 = "==3.8.3"

black = "==19.10b0"

[packages]

django = "==3.0.8"

If you want to use a different version of the django package and/or the dev packages, just change them to the version you want to use for your project whilst inside the Pipfile. 

Once you happy with the versions and packages you want to use enter the command (pipenv install --dev), this will install all packages including the dev packages. To only install packages without installing dev packages use the command (pipenv install).

Next use the command (pipenv graph) to view all the installed packages (dependicies).

# create setup file 

create file called (setup.cfg) under your project folder and copy and paste, every thing below into the setup.cfg file. You only need to this once for each project you create.

[flake8]

ignore = E203, E266, E501, W503

max-line-length = 88

max-complexity = 18

select = B,C,E,F,W,T4

[isort]

multi_line_output=3

include_trailing_comma=True

force_grid_wrap=0

use_parentheses=True

line_length=88

# Creating a Project in Django
To create a project in Django, enter the command (django-admin startproject project_name .). You can name your project anything you want e.g. (django-admin startproject RealEstateProject .). Also always remember to add a space at the end of the project_name then a dot after the space.

# Start an App within a project 
A Django project is made up made up of individual apps that make the project work as a whole. While in active virtual environment use the command (python manage.py startapp app_name) to start a app within your project.