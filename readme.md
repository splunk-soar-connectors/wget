[comment]: # "Auto-generated SOAR connector documentation"
# wget

Publisher: Aaron S\. DeVera  
Connector Version: 0\.1\.0  
Product Vendor: Generic  
Product Name: wget  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 3\.0\.284  

File acquisition app similar to wget functionality\. Saves any file at a targets URL to a container vault for further action\.


Replace this text in the app's **readme.html** to contain more detailed information


### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a wget asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**proxy domain** |  optional  | string | Option to route wget request via a proxy domain\.

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[get file](#action-get-file) - Acquires file at a target URL and saves to a container vault  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'get file'
Acquires file at a target URL and saves to a container vault

Type: **generic**  
Read only: **False**

Acquires file at a target URL and saves to a container vault\. Similar to wget functionality that allows for recursive downloads of web artifacts\.

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**target url** |  required  | URL location of the targeted file you intended to download | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.data\.\*\.vault\_id | string |  `vault id` 
action\_result\.parameter\.target url | string |  `url` 
action\_result\.status | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 