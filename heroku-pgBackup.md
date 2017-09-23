# Postgres DB Backup Workflow in Heroku
### 1. Create a new backup of your production db.
```
$ heroku pg:backups:capture --remote heroku
```

You should see the last line of the response as 
```
Backing up DATABASE to b004 ... done
```
__b004__ is your backup id/key which you need to take a note of. Your's might be something different.

### 2. Fetch the backup db URL.
```
heroku pg:backups:url b004 --remote heroku
```
You'll get a response with the URL for your backup db instance.


### 3. Download Backup into a dump file.
##### For Windows (Using PowerShell) 
```
> wget "URL" -OutFile yourBackupFileName.dump
```

##### For Mac or Linux Users
```
$ curl "URL" > yourBackupFileName.dump
```

### 4. Update your local db with the backup file
```
$ pg_restore --verbose --clean --no-acl --no-owner -h localhost -d [yourLocaldbName] yourBackupFileName.dump
```
