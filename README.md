# Linux commands

1. To add a content to a file with cat(redirect) . Run cat > /path/to/<filename> command
    ```bash
    cat > Africa/Egypt/Cairo/City.txt
    Cairo
    `Type Ctrl + d from keyboard`
    ```
2. Help commands
   ```bash
   whatis date
   man date
   ```
3. Alias
    ```bash
    date
    alias dt=date
    dt
    #To save it permanently
    echo alias up=uptime >> ~/.profile
    ```
4. Bash environment variables
   ```bash
   printenv
   export OFFICE=caleston
   echo $OFFICE
   ```
   To persistently set an environment variable over subsequent login or a reboot add them to the ~/.profile or ~/.pam_environment in the users home directory.
   ```
   echo "export OFFICE=caleston" >> ~/.profile (or)
   echo "export OFFICE=caleston" >> ~/.pam_environment
   ```
5. Searching
   ```bash
   find /home/michael -name City.txt
   grep -i "capital" sample.txt
   ```
6. Redirection
   ```bash
   echo $SHELL > shell.txt
   echo $SHELL >> shell.txt  #Append to file

   #Use 2>> to redirect error stream
   cat missing_file 2>> error.txt
   cat missing_file 2> /dev/null  #Don't print error message

   #Pipe will give output of first command as input to second command.
   echo "Hello World" | wc -w
   ```
