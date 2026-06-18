# AWS WordPress Backup & Recovery Commands

## Install Apache

```bash
sudo apt update
sudo apt install apache2 -y
```

## Install MySQL

```bash
sudo apt install mysql-server -y
```

## Install PHP

```bash
sudo apt install php php-mysql -y
```

## Create WordPress Database

```sql
CREATE DATABASE wordpress_db;
```

## Backup Database

```bash
sudo mysqldump wordpress_db > wordpress_backup.sql
```

## Restore Database

```bash
sudo mysql wordpress_restore < wordpress_backup.sql
```

## Verify Recovery

```sql
USE wordpress_restore;
SHOW TABLES;
```
