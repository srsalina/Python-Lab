# ALGORITHM FOR UPDATING FILES IN PYTHON

## Objective


This project demonstrates how I used Python to modify the contents of a file. I was given a hypothetical task to update a text file identifying which hospital employees could access restricted information regarding patient records. This file, named allow_list.txt, contained a series of IP addresses that were allowed to access the aforementioned patient records. The end goal was to develop an algorithm that could parse through any similar file and remove IP addresses that should no longer be allowed to access sensitive information. To achieve this, I used Python to parse through the allow_list.txt file and remove IP addresses that should no longer have access. This hands-on experience was designed to deepen my understanding of Python scripting and file manipulation concerning security. 

### Skills Learned


- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.



## Procedure
drag & drop screenshots here or use imgur and reference them using imgsrc


### Opening the File Containing the Allow List

To begin writing my algorithm, I first needed to import the access file, allow_list.txt, and save it to a variable. Saving it to the variable import_file, as seen in the capture below, facilitates future file manipulation. The hypothetical hospital provided me with the variable remove_list, which contained a list of IP addresses to be removed from the allow_list.txt access file. 

![image](https://github.com/srsalina/Python-Lab/assets/131724448/7de344aa-4981-411c-b02b-77c5ee749116)


*Ref 1: Network Diagram*
