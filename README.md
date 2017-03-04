
# Installation guide

1. Create a database on your server
2. Run the sql query to create messages table:

```
CREATE TABLE `ssm` (
  `id` varchar(160) NOT NULL,
  `pgp_key` longtext,
  `message` longtext,
  `created` timestamp NULL DEFAULT CURRENT_TIMESTAMP
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```

3. Copy `mysql_connection.SAMPLE.php`, and rename it to `mysql_connection.php`
4. Update `mysql_connection.php` with correct database host, user, password and name
5. Upload and test

## Keeping the database up to date

This part is missing. Some help is welcome:

Simplest solution is to create a database dump script that someone can import.

More complex and proper solution would be to allow anyone to submit url of their node, and have nodes communicate with each other. Still not difficult but at the moment I can't afford to spend so much time to programm this.