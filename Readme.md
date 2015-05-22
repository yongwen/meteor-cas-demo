A demo to use CAS authentication with Meteor accounts system, using:
https://atmospherejs.com/atoy40/accounts-cas

# Usage

add the accounts-cas package

$ meteor add atoy40:accounts-cas

start the server

$ meteor --settings settings.json

Note: You will need to allow the pop-up to see the cas login page.

# CAS with an "allowed_users" list

in the settings.json, there is a list of users defined in "allowed_users". If the user is not in the list, the login will failed with "user not in the allowed list" error.
You can add the username in the list, then restart the server using the above command.

If you want to remove a user from the list and the user had been logged in before, because the user had been created in the meteor system, 
you will need to reset the meteor DB or remove the user from Meteor. To reset the Meteor db and restart the server, do:

$ meteor reset
  
$ meteor --settings settings.json
