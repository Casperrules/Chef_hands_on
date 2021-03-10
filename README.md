# Chef_hands_on
contains solution to chef handson solutions
## Exercise - 1
### crontask cookbook:
the crontask cookbook contains a custom resource to create a cronjob in the VM that runs a shell file provided by the user. running this cookbook alone does not do anything
### testcron cookbook:
this cookbook uses the custom resource created in the crontask cookbook to create and test the working of the cron task successfully.
running this cookbook creates a cron job to run the /home/test.sh file every 30 minutes

## Exercise - 2
### bashcreater cookbook:
this cookbook contains recipes to create shell script to add user and group. Takes input from a json file in chef-client using a -j option. has libraries to fetch data from json file and two functions for creating list of users and groups in different files. the final execute resource is used to run a command that deletes files older than 59 minutes(1hour). the runcron recipe is used to create a cron job to run the script. the script in itself contains checks to make sure user and group are created only if not exist. 
