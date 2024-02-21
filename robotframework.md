# **Robot-Framework**   
![N|Solid](https://camo.githubusercontent.com/bad44edd183cbf659dbe484b982dbdb8381858354a2590533ddefecea70e696a/68747470733a2f2f6c68372d75732e676f6f676c6575736572636f6e74656e742e636f6d2f497a75656a4e414c5748457478437a64505a31345942764f386b756e35636f376f446478697043726b392d707967716f6a6a4768785a76574d692d634273686245364a5a39426e7666516e575f4f763068555f6b353841797850383762766d3532684b2d79667935565f5a32393030386779494a4f75623434392d56594464785076376d66496b736738414a6a307865705a4839506a41)

---

# Table of Content:-
- [Introduction](#introduction)
- [What is the Robot-Framework](#what-is-the-robot-framework)
- [Different Types of testing supported by Robot Framework](#different-types-of-testing-supported-by-robot-framework)
- [Setup of Robot-Framework](#setup-of-robot-framework)
- [Keywords in Robot-Framework](#keywords-in-robot-framework)
- [Variables in Robot-Framework](#variables-in-robot-framework)
- [My First Test Case](#my-first-test-case)
- [Second Test Case](#second-test-case)

- ---

# Introduction

Robot Framework is a generic open-source test automation framework that provides an easy-to-use, keyword-driven approach to automation. It is written in Python and allows users to create high-level test cases that can be easily translated into machine-executable automation scripts.
It follows different test case styles − keyword-driven, behaviour-driven and data-driven for writing test cases. Robot Framework provides support for external libraries, tools which are open source and can be used for automation.


---
# What is the Robot-Framework.

Robot Framework is a generic, Python-based, open-source automation framework. It can be used for test automation and robotic process automation (RPA).

Robot Framework is supported by Robot Framework Foundation. Many industry-leading companies use the tool in their software development.

Robocorp provides tools to write, execute and orchestrate software robots that are powered by Robot Framework to be used in RPA, so understanding the basics is fundamental for any Software Robot Developer.

Robot Framework is a generic test automation framework for acceptance testing and acceptance test-driven development (ATDD). It is a keyword-driven testing framework that uses tabular test data syntax.

---
# Different Types of testing supported by Robot Framework

Robot Framework is used when there is a need for test automation in a software development process. It is particularly useful in projects that require continuous integration and delivery, as it supports different types of testing and can be easily integrated with other tools such as Jenkins and Git.

Robot Test Framework is a versatile test automation framework that can be used in a variety of scenarios. Some common use cases for the Robot Framework include:

**Acceptance Testing:** Robot Automation Framework is often used for acceptance testing, which involves testing whether a software system meets the specified requirements. This type of testing can be done at various stages of the software development lifecycle, from early prototypes to final releases.

**Regression Testing:** Regression testing is used to ensure that software changes or updates do not introduce new bugs or issues. Robot Framework is a popular choice for regression testing because of its modular architecture and ability to easily reuse test cases.

**Functional Testing:** Python Robot Framework can be used for functional testing, which involves testing the functionality of a software system. This can include testing individual functions or components, as well as testing the system as a whole.

**Integration Testing:** Integration testing involves testing how different components of a software system work together. The Robot Framework can be used to automate this type of testing, allowing testers to easily test the interactions between different components.

**API Testing:** Robot Framework has built-in libraries for testing APIs, making it a popular choice for testing RESTful and SOAP web services.

---
# Setup of Robot-Framework
### Prerequisites: 
**Install Python
Install PIP 
Install PyCharm IDE  
Download Selenium Browser drivers for the browsers**

# Installation

## Step 1: Install Python

Robot Framework is operating system and application independent. It is implemented using Python which is also the primary language to extend it.

### Command:-

``` 
sudo apt install python3
```
### Output:-
Reading package lists... Done
Building dependency tree       
Reading state information... Done
python3 is already the newest version (3.8.2-0ubuntu2).
python3 set to manually installed.

### Verify Installation    

```
python3 --version
```

### Output:-

Python 3.8.10

## Step 2: Install pip
PIP is a package manager for Python packages, or modules.

### Command:-
```
sudo apt install python3-pip
```
### Output:-
python3-pip is already the newest version (20.0.2-5ubuntu1.10).


### Verify Installation
```
pip3 --version
```
### Output
pip 20.0.2 from /usr/lib/python3/dist-packages/pip (python 3.8)

## Step 3. Install Selenium

Selenium is an open-source suite of tools and libraries that is used for browser automation

### Command:-
```
 pip3 install selenium
```
### Output:-
Installing collected packages: exceptiongroup, h11, wsproto, sniffio, attrs, sortedcontainers, outcome, trio, trio-websocket, pysocks, urllib3, certifi, selenium

Successfully installed attrs-23.1.0 certifi-2023.11.17 exceptiongroup-1.2.0 h11-0.14.0 outcome-1.3.0.post0 pysocks-1.7.1 selenium-4.15.2 sniffio-1.3.0 sortedcontainers-2.4.0 trio-0.23.1 trio-websocket-0.11.1 urllib3-2.1.0 wsproto-1.2.0

### Verify Installation
```
pip3 show selenium
```
### Output
Name: selenium
Version: 4.15.2
Summary: None
Home-page: https://www.selenium.dev
Author: None
Author-email: None
License: Apache 2.0
Location: /home/aakash/.local/lib/python3.8/site-packages
Requires: trio, trio-websocket, urllib3, certifi
Required-by: robotframework-seleniumlibrary
 
## Step 4. Install Pycharm 
### Command:-
```
 sudo snap install pycharm-community --classic
```
### Output:-
pycharm-community 2023.3.2 from jetbrains** installed

## Step 5. Install Robot Framework
```
pip3 install robotframework
```
### Output:-
Collecting robotframework

  Downloading robotframework-6.1.1-py3-none-any.whl (699 kB)

  |████████████████████████████████| 699 kB 1.2 MB/s

Installing collected packages: robotframework

  WARNING: The scripts libdoc, rebot and robot are installed in '/home/aakash/.local/bin' which is not on PATH.

  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.

Successfully installed robotframework-6.1.1

## Step 6. Install Robot Framework Selenium
```
pip3 install robotframework-seleniumlibrary
```
### Output:-
Installing collected packages: robotframework-pythonlibcore, robotframework-seleniumlibrary

Successfully installed robotframework-pythonlibcore-4.3.0 robotframework-seleniumlibrary-6.2.0

## Step 7. Install Robot Framework-Datadriver -
```
pip3 install robotframework-datadriver
```
### Output:-
Collecting robotframework-datadriver

  Downloading robotframework_datadriver-1.9.0-py3-none-any.whl (52 kB)

  |████████████████████████████████| 52 kB 491 kB/s

Requirement already satisfied: robotframework>=4.0.2 in ./.local/lib/python3.8/site-packages (from robotframework-datadriver) (6.1.1)

Collecting Pygments

  Downloading pygments-2.17.2-py3-none-any.whl (1.2 MB)

  |████████████████████████████████| 1.2 MB 677 kB/s

Collecting docutils

  Downloading docutils-0.20.1-py3-none-any.whl (572 kB)

  |████████████████████████████████| 572 kB 792 kB/s

Installing collected packages: Pygments, docutils, robotframework-datadriver

  WARNING: The script pygmentize is installed in '/home/aakash/.local/bin' which is not on PATH.

  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.

  WARNING: The script docutils is installed in '/home/aakash/.local/bin' which is not on PATH.

  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.

Successfully installed Pygments-2.17.2 docutils-0.20.1 robotframework-datadriver-1.9.0

## Step 8. Install Required Packages in Pycharm:-
**1. Selenium**
**2. Robotframework**
**3. robotframework-seleniumlibrary**
    
![N|Solid](https://camo.githubusercontent.com/6e2fbf08bd93f778ff0f71699366441f92a6bc1a29b4edf58041334bd58b7076/68747470733a2f2f6c68372d75732e676f6f676c6575736572636f6e74656e742e636f6d2f4c713837756431664f564d7738662d374d505958766e726d506833716c554c5947384a55496752486247706a6b58396e5a67623970337144384947694436354e7575466e34464d3768366b7957726a317a657a6d36567539635971324e77374d5a543457694f5438336a337249306447464967696778597a7068526e63557a4d4648624f303247393353713448597758476c68426c4b41)


---
# keywords in Robot-Framework    
    
Think of a keyword as a single test step. Just as a test is conceptually made up of many steps, a robot test is made up of many keywords.

There are generic keywords provided by robot, and there are special-purpose keywords that you can create yourself.    
    
##    Adding keywords to your robot script
You can add keywords to your script in two ways:

Library keywords: Importing a library by adding it to your   *** Settings *** section will allow you to use all keywords contained in the library. You can also create your own custom library.
User keywords: You can write your own keywords in a *** Keywords *** section in your script.

### User keywords with arguments
**To make the keyword more reusable, you can pass arguments to it by adding the [Arguments] setting to the keyword:**
```
*** Keywords ***
Take a screenshot of a web page
    [Arguments]    ${url}
    Open Available Browser    ${url}
    Capture Page Screenshot
```
**You can then call your keyword inside a task, or another keyword:**
    
```
*** Tasks ***
Take screenshots
    Take a screenshot of web page    https://www.google.com
    Take a screenshot of web page    https://www.robocorp.com
```    

**You can also specify more than one argument, and default values:**
```
*** Keywords ***
Perform a search on a search engine
    [Arguments]    ${search_url}=https://google.com/?q=    ${search_term}=robocorp
    Open Available Browser    ${search_url}${search_term}
```
**You could then call this keyword in your task like this:**
```
*** Tasks ***
Search using different search engines
    # No arguments passed, use the default, searching on Google for "robocorp":
    Perform a search on a search engine
    # Search for "rpa" on "duckduckgo":
    Perform a search on a search engine    https://duckduckgo.com/?q    rpa
```

#   Variables in Robot-Framework.
**Primarily there are 4 types of variables in Robot Framework –**

**1. Scalar (Identifier: $)** – The most common way to use variables in Robot Framework test data is using the scalar variable syntax like ${var}. When this syntax is used, the variable name is replaced with its value as-is.

**2. List (Identifier: @)** – If a variable value is a list or list-like, a list variable like @{EXAMPLE} is used. In this case, the list is expanded and individual items are passed in as separate arguments.

**3. Dictionary (Identifier: &)** – A variable containing a Python dictionary or a dictionary-like object can be used as a dictionary variable like &{EXAMPLE}. In practice, this means that the dictionary is expanded and individual items are passed as named arguments to the keyword.

**4. Environment (Identifier: %)** – Robot Framework allows using environment variables in the test data using the syntax %{ENV_VAR_NAME}. They are limited to string values.

# First Test-Case 
## where i open Github

 
#####  Create a file under ‘Tests’ folder with .robot extension. The .robot files are considered as Test Suites by Robot Framework.
![Screenshot of My Application](../../Pictures/Screenshot%20from%202024-02-21%2022-09-19.png)

## Robot File:-
``````
*** Settings ***
Library    SeleniumLibrary
Resource    ../Resources/LogIn_Resources.robot
Suite Setup    Open My Browser
Suite Teardown    Close Browsers
Test Template      Invalid User
``````

``````
*** Test Cases ***        username        Password
Right username empty Password        Aman-Sharma-au49        ${EMPTY}
Right username Wrong Password        Aman-Sharma-au49        aman
Wrong username empty Password        Aman-Sharma       ${EMPTY} 
Wrong username Wrong Password        Aman-Sharma        vats
Empty username empty password        ${EMPTY}        ${EMPTY}
#Right username Right password        Aman-Sharma-au49        Aman@639
   Sleep    3
   ``````

``````   
*** Keywords ***
Invalid User
   [Arguments]    ${username}    ${Password}
   Input Username       ${username}
   Input pwd       ${Password}
   Click Login Button
   Error Massege Should be visible
``````


## Resources Files:-

``````
*** Settings ***
Library    SeleniumLibrary
``````

``````
*** Variables ***
${logURL}        https://github.com/login
${Browser}        Chrome
``````

``````
*** Keywords ***
Open My Browser
   Open Browser        ${logURL}        ${Browser}
   Maximize Browser Window
Close Browsers
   Close All Browsers
Open Login Page
   Go To    ${LOGIN URL}
Input Username
   [Arguments]    ${username}
   Input Text    name:login        ${username}
Input pwd
   [Arguments]    ${Password}
   Input Text    name:password       ${Password}
Click Login Button
   Click Element    xpath://*[@id="login"]/div[4]/form/div/input[13]
Click logOut Button
   Click Link    logOut
Error Massege Should be visible
   Page Should Contain    Incorrect username or password
Dashbord Page Should be visible
   Page Should Contain    Dashbord
``````   

# Second Test Case 
## where i open My BMI localhost port

``````
*** Settings ***
Library    SeleniumLibrary
Suite Setup    Open Chrome Browser
Suite Teardown    Close Browser
``````

``````
*** Variables ***
${LOCALHOST_URL}    http://localhost:5173
${MAXIMIZE_TIME}    50s
``````

``````
*** Test Cases ***
Open Localhost 5173 and Maximize Window
    [Documentation]    Test case to open a local web application running on localhost port 5173 and maximize window
    Go To    ${LOCALHOST_URL}
    Maximize Browser Window
    Sleep    ${MAXIMIZE_TIME}
``````

``````
*** Keywords ***
Open Chrome Browser
    Open Browser    about:blank    Chrome
``````