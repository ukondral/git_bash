# Работа с git и bash

## Bash
Bash scripts are used for a range of tasks, from simple commands to complex programs with conditional operations, loops, and function calls. Working through the command line makes it easier and faster for the user to interact with the system, without using a GUI.
      Commands for working with files and folders:

### Task 1
cd ~                                     # Open the home directory
pwd                                      # Determine the name of the folder you are in
mkdir test1                              # Create a directory inside this folder named test1 
ls -l                                    # Checking if a folder has been created
cd test1                                 # Go to the folder test1
touch file{1,2,3}.txt                    # Create file 1,2 and 3 inside the directory test1
ls -l                                    # Checking the contents of the catalog test1
cd ~                                     # Go to home directory
mkdir test2                              # Create inside the home directory folder test2
rmdir test2                              # Delete the folder test2
cd ~/test1                               # To go to the folder test1
rm file2.txt                             # Delete File2
mkdir ~/test3                            # Create in the home directory a folder test3
touch file{4,5}.txt                      # Create file 4,5
cd ~                                     # Open the home directory
rm -r test3                              # Delete folder test3
ls -l                                    # check the deletion of the folder
mkdir ~/test4                            # Create in the home directory a folder test4
mv ~/test1/file{1,3}.txt ~/test4/        # Move files 1 and 3 from the folder test1 to the folder test4 
ls -l ~/test4                            # Check the contents of the folder test4
echo "line" >> file1.txt                 # Add three lines with the words line to file1
echo "line" >> file1.txt
echo "line" >> file1.txt
cat file1.txt                            # Check the contents of the file1
echo "line" >> file3.txt                 # Add three lines with the words line to file3
echo "line" >> file3.txt
echo "line" >> file3.txt
cat ~/test4/file1.txt ~/test4/file3.txt  # View the contents of files (file1.txt and file3.txt) at once
nano ~/test4/file1.txt                   # Replacing the lines in file1.txt


### Task 2
cd ~                                     # Open the home directory
pwd                                      # Determine the name of the folder you are in
mkdir test3                              # Create a folder test3
cd test3                                 # Go to test3
touch 4 5 6                              # create files 1, 2, 3
echo -e "row1\nrow2\nrow3\nrow4" > 4     # Add 4 "row" lines to each file
echo -e "row1\nrow2\nrow3\nrow4" > 5
echo -e "row1\nrow2\nrow3\nrow4" > 6
grep "row2" 5                            # Find row 2 in file 5
grep -r "row"                            # Find the "row" in the folder test3
grep -c "row" 6                          # Calculate how many lines with row in a file 6
find . -name "5"                         # Find file 5 inside the folder test3 
find . -name "5" -exec rm {} \;          # Delete file 5 using find
ls -l                                    # Сheck for deletion
echo "test" > 4                          # Add the word test to file 4 (without saving its contents)
cat 4                                    # Check the content
sed -i '' 's/test/fail/' 4               # Replace the word "test" with fail in file 4
echo "test" >> 4                         # Add the word test to file 4, saving the contents
ps aux                                   # View all processes for users (not only console ones)
kill 666                                 # Kill process 666
ping rusau.net                           # Check availability rusau.net using ping
ping -c 5 rusau.net                      # Send 5 packages to rusau.net

                                         # Using GET and the curl command, you can get information about registered pets with any status on https://petstore.swagger.io/

curl -X GET "https://petstore.swagger.io/v2/pet/findByStatus?status=available"    

                                         # Using PAST and the curl command, create a new user on https://petstore.swagger.io/

curl -X POST "https://petstore.swagger.io/v2/user" \
     -H "Content-Type: application/json" \
     -d '{"id":123, "username":"testuser", "firstName":"John", "lastName":"Doe", "email":"john.doe@example.com", "password":"123456", "phone":"1234567890", "userStatus":1}'
     




