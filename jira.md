* jira

  ```
  mysqldump -uroot -p --default-character-set=utf8 -d jira636>createdb.sql
  mysqldump -uroot -p --quick --no-create-info --extended-insert --default-character-set=latin1 jira636>data.sql
  mysql -uroot -p jira636 < createdb.sql
  mysql -uroot -p jira636 < data.sql

  create database confluence default charset utf8;
  GRANT ALL ON confluence.* TO jira_user@'%' IDENTIFIED BY 'jira_user123456';
  ```

  ​