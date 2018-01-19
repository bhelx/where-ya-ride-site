## WYR Site

This is a Jekyll site meant to be hosted on Github Pages.
It will eventally contain all web content for the WYR mobile app.
Right now it's being used to distribute GTFS databases to the mobile clients.

## Migrations

The clients will call `/mobile/migrations.json` to get a list of databases.
They will determine the latest database and fetch it. The format will allow for
GTFS schedules that start in the future (they will be pre-downloaded and ready for the client offline).
The format of migrations.json looks like this:

```json
{
  "migrations": [
    {
      "uploaded_at": "2018-01-15T00:00:00Z",
      "begins_at":  "2018-01-15T00:00:00Z",
      "url": "/mobile/databases/GTFS-2018-01-15T00:00:00Z.sqlite.gz"
    }
  ]
}
```
