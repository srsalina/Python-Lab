# ALGORITHM FOR UPDATING FILES IN PYTHON

## Objective


This project demonstrates how I used Python to modify the contents of a file. I was given a hypothetical task to update a text file identifying which hospital employees could access restricted information regarding patient records. This file, named allow_list.txt, contained a series of IP addresses that were allowed to access the aforementioned patient records. The end goal was to develop an algorithm that could parse through any similar file and remove IP addresses that should no longer be allowed to access sensitive information. To achieve this, I used Python to parse through the allow_list.txt file and remove IP addresses that should no longer have access. This hands-on experience was designed to deepen my understanding of Python scripting and file manipulation concerning security. 

### Skills Learned


- Proficiency in using with statements to open, read, and write files using the open() function in Python, ensuring efficiency.
- Developed an algorithm to parse and update file contents through iteration and conditionals, demonstrating problem-solving skills in a cybersecurity context.



### Tools Used
- Utilized Jupyter Notebook to write and debug Python, making it easier to visualize the workflow and results
- Python programming language



## Procedure


### Opening the File Containing the Allow List

To begin writing my algorithm, I first needed to import the access file, allow_list.txt, and save it to a variable. Saving it to the variable import_file, as seen in the capture below, facilitates future file manipulation. The hypothetical hospital provided me with the variable remove_list, which contained a list of IP addresses to be removed from the allow_list.txt access file. 

![image](https://github.com/user-attachments/assets/015fecf5-a85a-4ef4-9c11-d784c2a0bfa9)

The first step in writing my algorithm was to view the allowed IP addresses stored in the imported file. I used a with statement combined with the open() function to open the file in read mode. Using the with keyword closes files after exiting the statement, saving system resources and time. The open() function takes in two parameters: the file to be opened and the action to be applied. I used the import_file variable for the first parameter and “r” for the second, indicating that I want to open the file only to read it. After the closing parameters of the open function, the as keyword saves the function's output to a variable of our choosing (named file for simplicity). This variable is scoped to the with statement and can be used within it.

![image](https://github.com/user-attachments/assets/7427f382-438e-4198-815a-9c41bdeea4de)


### Reading the Contents

I used the .read() method on the variable file to read the contents. The .read() method outputs a string, which I saved to a variable named ip_addresses. The original file's contents were now in a string I could manipulate. 

![image](https://github.com/user-attachments/assets/6d482847-932f-4854-b3a4-22e2838a5d5b)


### Converting the string into a list

To remove the unwanted IP addresses, the ip_addresses variable needed to be in a list format that I could quickly iterate through. I used the .split() method to turn the original file's content into a list. The screenshot below demonstrates how I did this. 

![image](https://github.com/user-attachments/assets/9563a30a-9f4f-4170-990a-a920ce5ba970)


### Using Iteration to Remove Unwanted IP Addresses

Once I had a list of the allowed IP addresses saved to a variable, my objective was to iterate through the list using a for loop and remove any IP addresses that matched an IP address from the remove_list. I wrote an if conditional within my for loop, as shown below. 

![image](https://github.com/user-attachments/assets/75f22d56-c45b-48fd-b156-b6c4d12444a8)


### Updating the file with the revised list of IP addresses 

After removing the unwanted IP addresses from my list, the next step was to update the original file saved as the variable import_file. Before doing this, however, I needed to revert my updated list to a string. A line of code containing the .join() method has been added to the code to update the file. This is necessary because ip_addresses must be in string format when used inside the file with a statement to rewrite it.

![image](https://github.com/user-attachments/assets/9c19595b-b257-4245-a6ff-6fed8fabdb33)


Then, I used another with statement to open the import_file in write mode. I used “w” as the second argument this time to indicate that I wanted to open the file to write over its content. As seen below, I used the .write() method to overwrite the contents of the original import_file with the newly updated allowed IP addresses saved in the variable ip_addresses. 

![image](https://github.com/user-attachments/assets/552efad6-4cf9-4858-bf3a-e72ad0204bcb)


### Wrapping it All Up in a Reusable Function 

I started by defining the function's name as update_file and allowing it to take two parameters: the file to be modified and the list of IP addresses to be removed. Next, I added the initial with statement that copies the contents of the import file to a variable and the line of code, ip_addresses = ip_addresses.split(), that turns that variable into a list. I also added the for loop that removes the unwanted IP addresses from the list and the line of code, ip_addresses = “ “.join(ip_addresses), that returns the list into a string. Finally, I added the last with statement that overwrites the import file with the updated list of allowed IP addresses. The full function is shown in the screenshot below. In creating this function, I made a reusable algorithm that can be used for similar purposes in the future.

![image](https://github.com/user-attachments/assets/c769119f-e3c3-44c9-a52d-eddcaa05643b)

The function can be used as shown below. 

![image](https://github.com/user-attachments/assets/49fc3b2a-5347-4624-a370-f203a3eab6fb)



## Summary 

In this project, I demonstrated how Python can be used to automate tasks related to cyber security. I created a reusable algorithm that can be used for file manipulation tasks, such as preventing unwanted IP addresses from accessing private patient files. This project highlights my ability to solve real-world security tasks using programming skills.

