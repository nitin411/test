## Project Description <br />
This project automatically detects URLs present in Jira issue, check them in PAC file and block them on Zscaler 
followed by a confirmation on Jira
### Prerequisite <br />
You should have a Jira and Zscaler account, make changes in the config.ini file accordingly. <br />
Passwords in the config.ini file should be Base64 encoded
### Commands to execute <br />
   Go to the specific folder location <br />
```$pipenv shell 3``` (creates a virtual environment) <br />
    copy webhook_request.py , url_block_zscaler.py , config.ini and setup.py to that folder <br />
```$python setup.py install``` <br />
```$export FLASK_APP=webhook_request.py``` <br />
```$flask run --host=0.0.0.0 ```(to make localhost listen to public requests) <br />
   To execute the program, send a post Jira issue request to the generated flask URL through the webhook 
   option provided on Jira. <br />
