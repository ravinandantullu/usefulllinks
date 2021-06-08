MY SQL root password reset steps:

Go to services and stop the mysql service in windows

Then create a txt file with the below command and save the file
alter user 'root'@'localhost' identified by 'Password that you intended to reset'

For examples saved the file to c:/change.txt

Load command prompt as Administrator 
Go to bin folder wher mysql was installed
Example:
C:\Program Files\MySQL\MySQL Router 8.0\bin

Now unhide the programdata under c drive and get the below path 
C:\ProgramData\MySQL\MySQL Server 8.0\my.ini

Execute this in command prompt
mysqld --defaults-file="C:\ProgramData\MySQL\MySQL Server 8.0\my.ini" --init-file="C:\Source\change.txt" --console

Which starts the mysql service, so close this window or exit this service

Now go to the service and start the mysql service.
Now start the service.
