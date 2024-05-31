# CucumberDemoProject

Behavior-Driven Development (BDD) is a development approach that involves writing tests in a natural language that non-programmers can read. In Python, the behave library is commonly used for BDD. To create a BDD setup using Python with Eclipse as the IDE, Please follow these steps:

1. Install Python and Behave
Install Python: Make sure Python is installed on your system. You can download it from python.org.
Install Behave: Install the behave library using pip. Open a terminal or command prompt and run:

pip install behave

2. Install Eclipse and PyDev
Download and Install Eclipse: Download Eclipse from eclipse.org and install it on your system.

Install PyDev:

Open Eclipse.
Go to Help -> Eclipse Marketplace.
Search for PyDev and install it.
Restart Eclipse after the installation is complete.
3. Set Up a Python Project in Eclipse
Create a New Project:

Open Eclipse.
Go to File -> New -> Project.
Select PyDev Project and click Next.
Name your project and configure the interpreter if necessary.
Click Finish.
Configure the Project for Behave:

Create a directory structure for your BDD tests. The typical structure is:

your_project/
├── features/
│   ├── steps/
│   │   └── steps.py
│   └── example.feature
└── src/

4. Write Feature Files
Create a Feature File:

Right-click on the features directory in Eclipse and select New -> File.
Name the file example.feature and click Finish.

Write a Scenario in the Feature File:

Feature: Example feature
  Scenario: Simple scenario
    Given I have a configured BDD environment
    When I write a scenario
    Then I should be able to run it
5. Write Step Definitions
     1.   Create a Step Definition File:
          Right-click on the steps directory in Eclipse and select New -> File.
          Name the file steps.py and click Finish.

     2. Implement Step Definitions:
        go to steps.py.  
        
6. Run the BDD Tests
Run the Tests from the Command Line:
Open a terminal or command prompt.
Navigate to your project directory.
Run the following command to execute the test
behave

Run the Tests from Eclipse:

You may need to configure Eclipse to run Behave tests. This can be done by creating a run configuration that executes Behave.
Go to Run -> Run Configurations.
Create a new configuration for Python and set the script to the Behave executable.
Configure the working directory and arguments as needed.
By following these steps, you can set up a BDD environment using Python and Eclipse, allowing you to write and execute tests using the Behave library.

output - Running Steps.py from Commandline using pytest

D:\Eclipse-workspace\CucumberDemoProject\features\steps>pytest -s -v steps.py

platform win32 -- Python 3.12.0, pytest-8.2.1, pluggy-1.5.0 -- D:\Softwares\python 3.12\python.exe
cachedir: .pytest_cache
metadata: {'Python': '3.12.0', 'Platform': 'Windows-11-10.0.22631-SP0', 'Packages': {'pytest': '8.2.1', 'pluggy': '1.5.0'}, 'Plugins': {'anyio': '4.0.0', 'bdd': '7.1.2', 'html': '4.1.1', 'metadata': '3.1.1', 'reporter': '0.5.3'}}
rootdir: D:\Eclipse-workspace\CucumberDemoProject\features\steps
plugins: anyio-4.0.0, bdd-7.1.2, html-4.1.1, metadata-3.1.1, reporter-0.5.3
collected 1 item ( Test selected)  Make sure start the function name with Test .otherwise pytest won't pick it up.

steps.py::test_step_given_configured_environment PASSED

Running the feature files from commandline using Behave

D:\Eclipse-workspace\CucumberDemoProject\features>behave
Feature: Example feature # example.feature:20

  Scenario: Simple scenario                   # example.feature:21
    Given I have a configured BDD environment # steps/steps.py:3
    When I write a scenario                   # steps/steps.py:7
    Then I should be able to run it           # steps/steps.py:11

1 feature passed, 0 failed, 0 skipped
1 scenario passed, 0 failed, 0 skipped
3 steps passed, 0 failed, 0 skipped, 0 undefined
