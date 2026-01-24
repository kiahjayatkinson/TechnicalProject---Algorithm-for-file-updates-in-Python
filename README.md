# Algorithm for file updates in Python

## Project Description
You are a security professional working at a health care company. As part of your job, you're required to regularly update a file that identifies the employees who can access restricted content. The contents of the file are based on who is working with personal patient records. Employees are restricted access based on their IP address. There is an allow list for IP addresses permitted to sign into the restricted subnetwork. There's also a remove list that identifies which employees you must remove from this allow list. Your task is to create an algorithm that uses Python code to check whether the allow list contains any IP addresses identified on the remove list. If so, you should remove those IP addresses from the file containing the allow list. 

### Open the file that contains the allow list
The file containing the permitted employee IP addresses (allow_list.txt) must be opened in read mode ("r") to access its contents: 
<img width="601" height="69" alt="1" src="https://github.com/user-attachments/assets/36e1d226-b95d-4490-bb87-b5cfe28e7d25" />

### Read the file contents 
The entire contents of the allow list file are read into a single string variable (ip_addresses): 
<img width="595" height="70" alt="2" src="https://github.com/user-attachments/assets/dad7c99f-cf39-45e1-9e83-ef77c4de2700" />

### Convert the string into a list 
The string containing all IP addresses is converted into a list of individual strings using the .split() method: 
<img width="593" height="59" alt="3" src="https://github.com/user-attachments/assets/ea752847-8999-42b3-a13c-c20217032198" />

### Iterate through the remove list 
A for loop is initiated to iterate over the items in the ip_addresses list. To safely remove elements within the loop, the iteration is performed over a copy of the list: 

<img width="607" height="67" alt="4" src="https://github.com/user-attachments/assets/902fff01-0684-4d0f-ad3a-3e793620103b" />

### Remove IP addresses that are on the remove list 
A conditional if statement checks if the current element (IP address) exists within the remove_list. If a match is found, the IP address is removed from the original ip_addresses list using the .remove() method: 
<img width="622" height="87" alt="5" src="https://github.com/user-attachments/assets/45a5515c-10d8-42e2-8e36-cc9de673960b" />

### Update the file with the revised list of IP addresses  
To finalize the update, the filtered list is converted back into a single, space-separated string using the .join() method. The original file is then opened in write mode ("w") to overwrite its entire content with the revised list. 
<img width="622" height="144" alt="6" src="https://github.com/user-attachments/assets/5030b2e6-b707-4117-bece-dd1ef8c775b6" />

## Summary
The entire logic is encapsulated into a reusable Python function, This function automates the security task of ensuring only currently authorized employees have IP access to the restricted subnetwork containing personal patient records. 

### Here is the entire Python code as a whole below: 
<img width="690" height="363" alt="All" src="https://github.com/user-attachments/assets/4d5d447f-901d-4d56-a086-287fe9f2bbdf" />





