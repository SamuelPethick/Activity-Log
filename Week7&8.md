# Week 7 Activity Log
## Objective: Set up a VM (Virtual Machine)

### Feburary 22nd 2023

Time worked on: 30 minutes

Requirements: A $50 credit in google cloud, on the account used. Or alternative method of payment. Work on this website https://console.cloud.google.com/getting-started

Accomplishments and Outputs: Creating a VM for ArcGIS server that allows port access to an administrative port.

Steps Taken:

1. Create a New project
2. Enable the Compute Engine API, which can be located from your project overview (Use cntrl f to help locate it.) Except this process to take a few minutes.
3. From the Compute Engine VM instances, interface click, create instance. (Take note of the status field which indicates if it is running, important to monitor considering it costs money.)
4. Give it an appropriate name then, change the bootdisk, within the bootdisk select custom image, from here view all and change the source to Shawn's ArcGIS server, then select the image that is available from this source.
5. Next change the firewall to allow HTTP and HTTPS acces (ports 80 and 443 respectively), note after this is created the VM has to be edited to allow traffic from port 444.
6. After the VM is created select "setup firewall rules" then click "create firewall rule", under "Target" use the dropdown menu and select "all instances in this network" then locate "Source IPv-4" ranges and input "0.0.0.0/0" then go to the "protocals and ports" section, under "specified protocols and ports" under TCP ports input "444" finally click create to finish the firewall rule.
7. Next we need to set login credentials. To do this, navigate back to the VM instances under Compute Engine. Click the arrow next to RDP, under the connect field and click set windows password. From here set the username to "student" and copy the password keeping it in a safe space.
8. To connect to the VM naviagte to remote desktop connection in file explorer.
9. Select the External IP which is located in the Compute Engine VM instances menu. Paste the IP into remote desktop connection adding port ":444" on the end.
10. It will then prompt for credentials, select more choices, then use a different account, enter the user name "student" and the password you saved earlier.
11. You will get a firewall warning but since you are the author you know you can accept it.
12. After connecting you can close it by pressing the X on the top bar on the VM.
13. Remember to stop the VM instance from the Computer Engine VM instances menu before leaving.

Next Steps: Creating a server on the VM and uploading to it.

### March 3rd 

Time worked on: 45 minutes

Requirements: A VM.

Accomplishments and Outputs: Creating an ArcGIS server on the VM and uploading a shapefile to it from ArcGIS Pro.

Steps Taken:

1. Start the VM on Compute Engine.
2. Setup a domain/url on DuckDNS. 
3. Update the IP on the domain to the external IP from Compute Engine.
4. Conncet to the VM.
5. On the VM create this file path C:\GISWorkspace and put the Canada.zip folder into it. Then extract.
6. Open ArcGIS Pro, make a connection to the DuckDNS domain through ArcGIS Server. Use the logins from the text file on the VM.
7. Login to ArcGIS server manager on the VM, using the logins from the text file, and make a folder for the file. 
8. Back on ArcGIS Pro upload the shapefile to the server being sure to refresh the server after the folder creation.
9. After uploading shapefile navigate to its rest endpoint and use this as a reference to upload it on AGOL.
