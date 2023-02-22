# Week 7 Activity Log
## Objective: Set up a VM (Virtual Machine)

### Feburary 2nd 2023

Time worked on: 30 minutes

Requirements: A $50 credit in google cloud, on the account used. Or alternative method of payment. Work on this website https://console.cloud.google.com/getting-started

Accomplishments and Outputs:

Steps Taken:

1. Create a New project
2. Enable the Compute Engine API, which can be located from your project overview (Use cntrl f to help locate it.) Except this process to take a few minutes.
3. From the Compute Engine VM instances, interface click, create instance. (Take note of the status field which indicates if it is running, important to monitor considering it costs money.)
4. Give it an appropriate name then, change the bootdisk, within the bootdisk select custom image, from here view all and change the source to Shawn's ArcGIS server, then select the image that is available from this source.
5. Next change the firewall to allow HTTP and HTTPS acces (ports 80 and 443 respectively), note after this is created the VM has to be edited to allow traffic from port 444.
6. After the VM is created select "setup firewall rules" then click "create firewall rule", under "Target" use the dropdown menu and select "all instances in this network" then locate "Source IPv-4" ranges and input "0.0.0.0/0" then go to the "protocals and ports" section, under "specified protocols and ports" under TCP ports input "444"
7. 

Next Steps:

