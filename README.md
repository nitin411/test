# test

This project automatically detects URLs present in Jira issue, check them in PAC file and block them on Zscaler 
followed by a confirmation on Jira

You should have a Jira and Zscaler account, make changes in the config.ini file accordingly.
Passwords in the config.ini file should be Base64 encoded

Procedure to run the program:
    Go to the specific folder location
$pipenv shell 3 (creates a virtual environment)
    copy webhook_request.py , url_block_zscaler.py , config.ini and setup.py to that folder
$python setup.py install
$ export FLASK_APP=webhook_request.py
$flask run --host=0.0.0.0 (to make localhost listen to public requests)
    To execute the program, send a post Jira issue request to the generated flask URL through the webhook 
    option provided on Jira.
