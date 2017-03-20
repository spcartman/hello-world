# Test Assignment for Senior QA Engineer Position

## Overview
Test assignment consists of 2 parts:
- test cases creation for specified application
- automation of selected tests

Test cases are located in **test_cases** folder. Automation part of the assignment is described below.

## Implementation Details

The following instruments were used to accomplish automation part:
- *Python 3.5.2*
- *pytest 3.0.7*
- *Selenium 3.3.1*

The following tests were covered by automation scripts:
- items creation
- items modification
- items deletion
- items details verification

Please note that automation tests provided within this assignment cover positive cases. The main reason of the automation assignment is to demonstrate the ability to automate tests, code styling, approach, architectural solution, etc.

In addition I'd like to note that the appliction under test serves for demo purposes with no strict validations and lack of specification. Keeping this in mind all documented test cases were created with an assumption that the application functions as designed (email validation is an example of such assumption; it was assumed that the application demonstrates authentication facilities and lack of email validation is done on puspose). At the same time in real project a lot of defects/questions would have been raised if such issues occurred (like in the previous example with email validation).

## Requirements
In order to run the tests you need to have the below requirements to be satisfied:
- latest *Python 3* (can be downloaded from official Python [website](https://www.python.org/)); make sure *Python* is added to environemnt variables
- latest *pytest* (can be install in terminal with *Python* package manager *pip*: `pip install pytest`); make sure *pytest* is added to environemnt variables
- latest *Selenium* (can be install in terminal with *Python* package manager *pip*: `pip install selenium`)

Tools needed to run the tests are also specified in **requirements.txt** file. Once *Python* is installed you can install other tools by running in terminal `pip -r PATH_TO_PROJECT_FOLDER/requirements.txt`.

In order for tests to launch browsers you need to have corresponding **drivers** available on your machine (can be downloaded from Selenium [download page](http://www.seleniumhq.org/download/)). Make sure the path where drivers are located is added to environemnt variables. In presented solution the following browsers are supported: *Chrome*, *Firefox* and *Internet Explorer*.

## Tests Execution
To execute tests run the following command in terminal:
- `pytest PATH_TO_PROJECT_FOLDER/test`
Another way to execute test is running in terminal:
- `python -m pytest PATH_TO_PROJECT_FOLDER/test`

The following **custom options** for test launch are supported:
- *--browser* which is used to specify browser for tests to run in; supported values: *chrome*, *firefox*, *ie*; *chrome* is default option; for example, to run tests in *firefox* run in terminal `pytest --browser=firefox PATH_TO_PROJECT_FOLDER/test`
- *--config* which is used to specify config file; takes path to config file as an input; by default *config.json* file located in project root folder is used
