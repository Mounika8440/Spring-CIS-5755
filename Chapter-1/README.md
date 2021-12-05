Code Management with Github

----------------------------------------------------
Github and Cloud9 setup using Personal Access Token:
----------------------------------------------------- 
Login Github and Create a repository
Click "Generate New Token" 
   a. Provide a Note such as "CIS5755"
   b. Select Expiration Date
   c. Select scopes
Click "Generate token", copy and paste the token in a temporary place
Create a new cloud9 environment
Delete the README.md file
git config --global credential.helper store
Go to Github and copy the repository URL
Go to Cloud9 terminal and clone the repository
  a. Type: git clone + repository URL
  b. enter your github username
  c. Copy and paste teh token for password
Change directory to the new folder
Create a project directory (e.g. mkdir Chapter-1)
Change to the new directory
Create python envionrment: python3 -m venv env
To activate the envionrment: source env/bin/activate
 Create a python file named ex1-print.py
Edit the python file
  a. Open the file
  b. Enter a line of code
  c. Run the file
While keeping the current terminal window for project,  open a new terminal for git to manage the source code) 

type git add --allin bash 
type git status in bash 
type git commit -m "first python code" in bash
  type git push
  a. github username:
  b. password: copy and paste the account access token
 check the changes by using: git log
Go to Github repository to check the changes
Go to Cloud9 and create a second python file: ex2-flask.py
Edit the file by copy/paste the basic Flask code
Save and Run the file
 In the terminal, install Flask package (library): python3 -m pip install flask
In the terminal, run the file: python3 ex2-flask.py
To view the app, go to Tools menu, select Preview --> Preview Running App
To stop the service, press Ctrl + C
 the git terminal, enter command step 17-21
   a. change commit comment to "First Flask example"

 Create an instruction markdown file for Chapter 1
   a. Edit the file by copy/paste this lab instructions
   b. Add basic markdown styles
   c. Save the file
 In the git terminal, enter command step 17-21
   a. change commit comment to "First Instruction File"


---------------------------------------------
Github and Cloud9 setup using SSH
-------------------------------------------
 Login Github and Create a repository
 get familiar with account profile --> settings 
 Create a new cloud9 environment
 Delete the README.md file
 Create ssh key for git to clone the project
ssh-keygen -t rsa
 Display the public key using cat command
 Copy the public key
 Go to github account settings --> SSH and GPG keys --> New SSH key 
 Paste the public key and enter a title
 Click "Add SSH key"
 Copy the repository URL
 Go to Cloud9 terminal and clone the repository
  a. Type: git clone + repository URL
  b. Yes

 Change directory to the new folder
 Create a project directory (e.g. mkdir Chapter-1)
 Change to the new directory
 Create python envionrment: python3 -m venv env
 activate the envionrment: source env/bin/activate
 Create a python file named ex1-print.py
 Edit the python file
  a. Open the file
  b. Enter a line of code
  c. Run the file
 While keeping the current terminal window for project,  open a new terminal for git to manage the source code) 
 git add --all
 git status
 git commit -m "first python code"
 git push
  a. github username:
  b. password: copy and paste the account access token

check the changes by using: git log
Go to Github repository to check the changes

-----------------------------------------------------------------

Basic Flask Code

from flask import Flask
app = Flask(__name__)
@app.route('/')
def hello_world():
   return 'Hello World'
if __name__ == '__main__':
    app.run(host='0.0.0.0', port=8080, debug = True)
