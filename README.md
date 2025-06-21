## Project description

An allow list of IP addresses is used at my company to manage access to content that is forbidden. These IP addresses are identified in the "allow_list.txt" file. The IP addresses that ought to be blocked from accessing this content are listed in a separate delete list. I developed an algorithm to automatically remove certain IP addresses that should not be able to access the "allow_list.txt" file and update it. 

### Open the file that contains the allow list

First, I opened the "allow_list.txt" file to begin the algorithm. Initially, I put this file name in the import_file variable as a string

<img src="https://i.imgur.com/5uVrPOz.png">

Then, I used a with statement to open the file

<img  src="https://i.imgur.com/lMKFwOD.png">

In my algorithm, the with statement is used with the .open() function in read mode to open the allow list file for the purpose of reading it.

### Read the file contents

In order to read the file contents, I used the .read() method to convert it into the string.

<img src="https://i.imgur.com/YhcXcdH.png">

this code reads the contents of the "allow_list.txt" file into a string format that allows me to later use the string to organize and extract data in my Python program

### Convert the string into a list

In order to remove individual IP addresses from the allow list, I needed it to be in list format. Therefore, I used the .split() method to convert the ip_addresses string into a list

<img src="https://i.imgur.com/2iGizyW.png">

The .split() function is called by appending it to a string variable. It works by converting the contents of a string to a list 

### Iterate through the remove list

A key part of my algorithm involves iterating through the IP addresses that are elements in the remove_list. To do this, I incorporated a for loop

<img src="https://i.imgur.com/hEqeMEu.png">

The for loop in Python repeats code for a specified sequence

### Remove IP addresses that are on the remove list

Any IP address that appears in remove_list and the allow list, ip_addresses, must be removed according to my method.  The reason I was able to accomplish this was because ip_addresses did not contain any duplicate addresses.

<img src="https://i.imgur.com/zVCzCn5.png">

### Update the file with the revised list of IP addresses

To do this, I first needed to convert the list back into a string. I used the .join() method for this

<img src="https://i.imgur.com/PjmWMJR.png">

The .join() method combines all items in an iterable into a string. 

Then, I used another with statement and the .write() method to update the file

<img src="https://i.imgur.com/GBX8jaA.png">

### Summary

I created an algorithm that eliminates IP addresses from the "allow_list.txt" file of permitted IP addresses that are found in a remove_list variable. This algorithm read the file, converted it to a string that could be read, and then turned the string into a list that was kept in the ip_addresses variable. After that, I went through each IP address in remove_list one by one. I determined whether the element was included in the list of IP addresses with each iteration. If so, I removed the element from ip_addresses using the .remove() method. Subsequently, I employed the .join() function to transform the IP addresses back into a string, enabling me to append the updated list of IP addresses to the "allow_list.txt" files contents.



















