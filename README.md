DeleteMail
==========

This simple Python Script allows you to delete mail from you pop3_ssl service in an automatic way, filtering on the From filer.

Usage: Just run 

python delmail.py 'keyword to filter' 'serverPOP3' 'username' 'password'

example: 
python delmail.py spamlord popmail.libero.it MegaNerd 12345
will delete a mail From: spamlord@site.com but not spam@lord.com from the account on Libero (an Italian mail provider) for the user MegaNerd which has password 12345 (which is accidentally the password of my luggage).

The script runs through all the mails, flags them for deletion and deletes the mails at the end of the script (so you can stop it if you change your mind before completion). Be careful: the script flags all the mails as "read", and if you have tons of mails it will take a lot of time. Mails will keep the "read" attribute even if you interrupt the script.

During execution, the script will display the id of the mail that is being deleted, so you can check the progress.

Requirements: You only need standard libraries: re (for filter), poplib (for accessing the pop3_ssl server), mail (to access the mail data).
