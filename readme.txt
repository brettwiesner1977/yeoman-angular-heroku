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

Setup
------


yo angular
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
heroku apps:create
git push heroku master
(failed)
ssh-keygen -t rsa -C “heroku”
heroku keys:add
git push heroku master
create a new repo on github (“heroku-proj-name”)
copy its location
go to heroku app page and in the settings add the username/heroku-prog-name.git to the github repo box
somewhere in some config file, add another url for this github, then push to heroku
