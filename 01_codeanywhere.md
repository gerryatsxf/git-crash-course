1. create a codeanywhere.com account

go to codeanywhere.com
create an account
for didactical purposes, preferred authentication mehtod are email+pwd or google auth

2. create an empty workspace

click the 'New +' button

in 'Git repository' select 'Codeanywhere-Templates/empty'

type a name for your new workspace

next: workspace will take a couple minutes (approx 10 min) to get created. this is the final result:

![alt text](image.png)

3. open a new termianl

go to burger menu at the top left of UI > terminal > new terminal

![alt text](image-1.png)

4. configure git

start by setting up your user so people know who made changes done in your machine

check current user config:
git config --global user.name
git config --global user.email

update user config:
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

5. create a new repository

a repository (repo) is a project folder tracked by Git.

let's start by creating a new folder using terminal: 

mkdir cryptotrading
cd cryptoptrading

run git init
This command git init creates a hidden .git folder where Git stores its history.



next, create a file named README.md using VSCODE WEB IDE or while in ./cryptotrading, run touch README.md

in it type the following text: this is the first version of my cryptotrading app




git status
git add .
git status
git commit -m "First version of my cryptotrading app"
git status
git log

Just to understand the commands:
git status: shows changes
git add: stages changes
git commit: saves a snapshot

6. start creating new commits

create a new file named app.py 

then in chatgpt ask the following:

hello chatGPT, please follow my instructions

1. create a very simple cryptotrading app
2. this app should run on a python fastapi server
3. it must serve a very simple static file with JS
4. this static file should graph the price of bitcoin up to last 30 days
5. make the UI very nice and appealing
6. this app should be a single app.py script
7. i must be able to run this by installing this very specific set of dependencies: pip install fastapi uvicorn requests
8. i must be able to run this script by executing command: uvicorn app:app 

copy chatgpt's output into app.py

check out the site you just created by runing uvicorn app:app in terminal

do ctrl+C to stop server


then run our usual workflow:

git status
git add .
git status
git commit -m "Bootstraped first version of web server"
git status
git log


7. create a new version

Git has branches feature. These are basically parallel versions of your files.

git branch solana
git checkout solana

next, open a fresh new chatgpt window
copy the contents of app.py in there, then ask chatgpt to update the code to graph the solana cryptocoin

prompt "update this to graph solana, return me the whole script, i must be able to easily copy it"

replace contents of app.py with the output

check out the updated site by runing uvicorn app:app in terminal


7. checkout back to master

so if you want to go back and run the bitcoin site again, you'll have to go back to master

git checkout master

check out the original site by runing uvicorn app:app in terminal