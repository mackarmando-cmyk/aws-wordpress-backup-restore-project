# AWS WordPress Architecture

## Architecture Overview

This project deploys a WordPress application on an AWS EC2 instance using a traditional LAMP stack.

## Architecture Flow

Internet  
↓  
AWS Security Group  
↓  
EC2 Instance  
↓  
Ubuntu Linux  
↓  
Apache Web Server  
↓  
PHP  
↓  
WordPress  
↓  
MySQL Database  
↓  
Database Backup  
↓  
Recovery Database  

## Diagram

```text
User / Browser
     |
     v
Public Internet
     |
     v
AWS Security Group
- SSH Port 22
- HTTP Port 80
     |
     v
EC2 Instance
Ubuntu Linux
     |
     v
Apache Web Server
     |
     v
PHP Runtime
     |
     v
WordPress Application
     |
     v
MySQL Database
wordpress_db
     |
     v
mysqldump Backup
wordpress_backup.sql
     |
     v
Restore Database
wordpress_restore

**Architecture Purpose**

The purpose of this architecture is to host a WordPress application in AWS while also validating database backup and recovery procedures.

**Key Design Decisions**
EC2 was used to simulate a traditional server migration.
Apache was used as the web server.
PHP was installed to support WordPress.
MySQL was used as the database layer.
Security Groups controlled public access.
mysqldump was used for backup and recovery validation.
Business Value

This architecture supports a basic cloud migration use case by moving a web application from a traditional server model to AWS. It also demonstrates business continuity by proving that the database can be backed up and restored if data loss occurs.
