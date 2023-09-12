# phpIPAM / AD User account synchronization

phpIPAM has no native tools for synchronization between local users and AD, therefore following solution should cover a gap.<br>
All users account for phpIPAM are stored locally in db but with different authentication methods.<br>

Available methods:  

![phpIPAM Auth](/phpIPAM-auth.png)

An idea is to have the same name (or almost) for each group in AD and phpIPAM, therefore the following groups has been created in phpIMAP

| phpIPAM | AD |
| :--- |  :--- |
| ad_phpIPAM_RO | phpIPAM_RO |
| ad_phpIPAM_RW | phpIPAM_RW |

Admin group has no mapping in AD but users are assigned to Administrators (Administrator level users)<br>
Script for synchronization is written in PHP as a native application is also a php-based, therefore no needs of any additional packages / software and no extra configuration is needed.<br>

Useful links:

- https://phpipam.net/
- https://github.com/phpipam/phpipam
- https://github.com/phpipam/phpipam/blob/master/db/SCHEMA.sql
