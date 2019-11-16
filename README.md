# edx-discussion board crawler

**edx-discussion board crawler** is a Python-based cross-platform tool for mining text data from discussion threads of the enrolled [edX](www.edx.org) courses available on a user's dashboard. THe edx discussion board is a dynamic page, thus we utilize the webdriver and selenium API to scrape the content. It was developed by teaching assistants at Tokyo Tech Online Education Development Office.

## Prerequisites
Python libraries and modules:

* [Python](https://www.python.org/downloads/) - version 3.5+
* [Selenium with Python](https://selenium-python.readthedocs.io/) - API to access webdriver
* [Chrome webdriver](http://chromedriver.chromium.org/downloads) - Chrome webdriver which requires the installation of official Chrome brower.  
## How to run
Before running, please make sure that the desired course(s) have already been listed in dashboard of your edx account.  
1) Download Chrome webdriver from the link provided at Prerequisites.
2) Add your edX account and password at "account info.json"
3) (Optional) add the desired edX course URLs in "course table.xlsx" 
4) open terminal and change a directory to the DB crawler folder 
5) Run a python script `edx-discussion.py` with the following command 

	'python edx-discussion.py'

6) The program will ask you the option for crawling.
-  type 1 and press enter if you want to manually select courses to be crawled
-  type any number and press enter if you want the program to crawl courses listed in course table.xlsx file
7) the crawler starts
	
The output is a JSON file ('all_dis2.json'), which is stored by default in "HTMLs\[COURSE_NAME]" folder .


## Extra files and folders
[DATETIME]_selected_file.csv contain the list of selected courses for crawling 

[DATETIME]_logfile_discussion.csv is the log file

## Test environment
Python 3.5, Windows 10 and Ubuntu 14 and 16
