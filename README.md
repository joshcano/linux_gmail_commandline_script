# linux_gmail_commandline_script
This is a very simple script I made to email myself or someone else a file with a bash terminal. 

Sending an email to yourself. 

    josh@server# gmail document.doc  
    sent document.doc myself@gmail.com 

Sending an email to someone else. 

    josh@server# gmail document.doc user@aol.com  
    sent document.doc to user@aol.com
   
## Set up is pretty simple. 
First, git the repository  

    git clone https://github.com/joshcano/linux_gmail_commandline_script.git  
    cd linux_gmail_commandline_script
    run bundler install

Now we need to edit the "app.rb" file and insert your email and password to gmail. There are numerous ways to do this, but you can do this in the script itself.

You need to edit line 4 and 5.   

    $user = "username@gmail.com"  
    $pass = "userpassword"  

then save the file  

Now we need to edit your .bashrc file.   
This will allow us to use 'gmail document.doc' from our command line.   

    josh@server# echo "alias gmail='ruby /path/to/app.rb'" >> ~/.bashrc  

Restart your bash session and send yourself a file!   

