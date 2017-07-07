## Uploading Database to Acquia

- drush sql-dump --gzip --result-file=../standardprofile.sql
- mysqldump -u root -proot drupal | gzip > standardprofile.sql.gz
- scp standardprofile.sql.gz jchs8.dev@free-6683.devcloud.hosting.acquia.com:./standardprofile.sql.gz
- ssh jchs8.dev@free-6683.devcloud.hosting.acquia.com
- drush @jchs8.dev ah-db-import ./standardprofile.sql.gz
