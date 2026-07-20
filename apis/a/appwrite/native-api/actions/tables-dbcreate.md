# Create database with Appwrite

Creates a new database in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create database](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | body | `string` | yes | Unique Id. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | body | `string` | yes | Database name. Max length: 128 chars. |
| `enabled` | body | `boolean` | no | Is the database enabled? When set to 'disabled', users cannot access the database but Server SDKs with an API key can still read and write to the database. No data is lost when this is toggled. |
