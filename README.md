This is the sendmail wrapper for linux bases servers 
Main purpose to build this .sh native wrapper for sendmail is to keep the logs of the emails in log files and along with store into some database via webhook and then pass the orignal mail along with all data without modifying to the Real/Actuall sendmail 

To implement this make the copy of existing running sendmail binary 
sudo mv /usr/sbin/sendmail.ssmtp /usr/sbin/sendmail.real

and update the code and then you see when ever server sends the mail from the MTA sendmail it will keep the log of the mails
It will store all php mails and cronjobs and system genrated mails as well 
