# aws-wordpress-backup-restore-project
AWS EC2 WordPress deployment with MySQL backup and disaster recovery validation.

# AWS WordPress Backup & Recovery Lab

## Project Overview

Deployed a WordPress application on AWS EC2 running Ubuntu, Apache, PHP, and MySQL.

Implemented a database backup and disaster recovery workflow using mysqldump and MySQL restore procedures.

## Architecture

AWS EC2
Ubuntu Server
Apache2
PHP
MySQL
WordPress

## Skills Demonstrated

- AWS EC2
- Linux Administration
- Apache Web Server
- MySQL Database Administration
- WordPress Deployment
- Database Backup & Recovery
- Troubleshooting

## Backup Command

sudo mysqldump wordpress_db > wordpress_backup.sql

## Restore Command

sudo mysql wordpress_restore < wordpress_backup.sql

## Verification

SHOW TABLES;

## Outcome

Successfully restored all WordPress tables into a recovery database and verified data integrity.
