hardening.cis-el7
=====================
This role will apply the CIS hardening for Rhel7 server and is made according to the v2.2.0 guidelines.  
Be carefull with this role as this will make a lot of changes to your server, proceed with caution.  
In the variables section below you will find some default variables like the section or task variables.  
If you don't want to apply a specific rule on your server, override those variables in your host_vars or group_vars.

Requirements
------------
/

Role Variables
--------------
Section specific enable/disable variables:  
**rhel7cis_section1**: CIS - General Settings  
**rhel7cis_section2**: CIS - Services settings  
**rhel7cis_section3**: CIS - Network settings  
**rhel7cis_section4**: CIS - Logging and Auditing settings  
**rhel7cis_section5**: CIS - Access, Authentication and Authorization settings  
**rhel7cis_section6**: CIS - System Maintenance settings  
**rhel7cis_section7**: CIS - Company specific settings


Task specific enable/disable variables:  
**rhel7cis_rule_1_1_1_1**  
**...**


**rhel7cis_bootloader_password**: Password to set on the bootloader  
**rhel7cis_set_boot_pass**: Configure the bootloader password or not  
**rhel7cis_time_synchronization_servers**: NTP timeservers that should be used  
**rhel7cis_warning_banner**: Login banner


**rhel7cis_tmp_mount_options**: Default options that will be placed on the mount of /tmp  


**rhel7cis_max_days**: Sets the max expiration days on a password  
**rhel7cis_min_days**: Sets the min days between password changes  
**rhel7cis_warn_age**: Sets a warning x days before the password will expire

Dependencies
------------
Ansible >= 2.7

Example Playbook
----------------
```
- name: Apply CIS hardening Rhel7
  hosts: all
  roles:
    - hardening.cis-el7
```
