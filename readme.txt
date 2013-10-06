yeoman-angular-heroku
=====================

This project is a barebones angular webapp built with yeoman and grunt, stored on github, and deployed on heroku.


Prerequisites
-------------
yeoman
grunt
yeoman generators
git and github account
node.js
heroku toolbelt and account
karma

Setup
------
All this should be done for the git bash shell
Install yeoman:
npm install -g yo
Install grunt and bower:
npm install -g grunt-cli bower
Install the angular generator:
npm install -g generator-angular
Install the heroku generator
npm install -g generator-heroku
Install karma:
npm install -g karma
npm install karma --save-dev  (installs karma locally)
npm install karma-ng-scenario --save-dev
npm install karma-firefox-launcher --save-dev
npm install karma-ie-launcher --save-dev
npm install karma-junit-reporter --save-dev
npm install grunt-karma --save-dev
Add the following env vars
CHRMOE_BIN=C:\Program Files (x86)\Google\Chrome\Application\chrome.exe
FIREFOX_BIN=C:\Program Files (x86)\Mozilla Firefox\firefox.exe
Git:
make a github account
add a key (https://help.github.com/articles/generating-ssh-keys)
ssh-keygen -t rsa -C “heroku”


Bootstrapping the project
-----------------
mkdir /c/dev/yeoman-angular-heroku
cd /c/dev/yeoman-angular-heroku
yo angular --minsafe
grunt
yo heroku (yes/ copy)
add to git (create a repo on github, then:)
touch readme.txt
git init
git add readme.txt
git add .
git commit -m "first commit"
git remote add origin https://github.com/brettwiesner1977/yeoman-angular-heroku.git
git push -u origin master
grunt
cd dist
git init
git add . 
git commit -m “my first commit”
heroku apps:create yeoman-angular-heroku
heroku keys:add ~/.ssh/id_rsa.pub
git push heroku master
create a new repo on github (“yeoman-angular-heroku”)
copy its location
go to heroku app page and in the settings add the brettwiesner1977/yeoman-angular-heroku to the github repo box

Making changes to the project, building the dist, committing to github and deploying to heroku
--------------------------------------------------------------------------------------------------
(make some code changes)
grunt
Add to github:
git commit -a -m "changed some stuff"
git push -u origin master
(now push to heroku)
cd dist
git init (dunno if needed)
git add .
git push heroku master