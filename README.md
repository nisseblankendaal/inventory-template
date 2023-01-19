# inventory-template
Template/example for our inventory structure
 
The inventory is based on a folder structure and ini files.
There are three main folders
 * group_vars
 * groups
 * host_vars
 
In the group_vars you will find a folder for every group. In this folder you can create (ini) files with variables for that specific group. Advised to group vars by creating seperate files per function/section. The vars for group "all" apply to all hosts if the specific var is not set in another group or host var.

In the groups folder you will find a folder per group with a members file. You'll have to add the hosts with their ansible inventory name in that members file. A host can be assigned to multiple groups and is automaticly a member for the group "all".

In the host_vars folder you will finf a folder per host with underneath one or more files with host specific variables like the ansible_host var.
