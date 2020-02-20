# Role Name:
- ansible-role-compliance-windows-advance-audit-logging-2016

# Description:
This Audit Logging Role was based off the CIS specs for 2016 servers.   This role covers the "Advanced Audit Policy Configuration" section only. The checks and remediations commands are for local settings only. Group Policy settings may override these settings. When the "remediate" variable is set to "YES", the role will try to remediate the server's setting(s) accoridng to the CIS standards.  The defaults/main.yml file can be used to disable specific CIS items (i.e. "execute_<cis task #>") from executing. The default value in the defaults/main.yml for these CIS item variables (i.e. "execute_<cis task #>") is set to "YES". The value "YES" means that the CIS item will execute at run time. Set the value to "NO" if you want to skip this CIS item in question from executing.

# Requirements:
Windows Ansible related pre-requisites 

# Variables:
Parameter | Choices/Defaults|Comments
----------|-----------------|--------
__remediate__ |"NO"| variable used to determine whether or not to remedaite.
__success_failure_cis__ |"Success and Failure"| CIS value.
__success_cis__ |"Success"| CIS value.
__failure_cis__ |"Failure"| CIS value.


# Example Playbook:
---
 - hosts: [win]
   roles:
   - ansible-role-compliance-windows-advance-audit-logging-2016


# Author Information:
Richard M. Williams (williamsitv@yahoo.com)
