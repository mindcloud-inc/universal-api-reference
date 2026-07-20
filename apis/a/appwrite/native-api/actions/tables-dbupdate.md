# Update database with Appwrite

Updates the database in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tablesdb/{databaseId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update database](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `name` | body | `string` | yes | Database name. Max length: 128 chars. |
| `enabled` | body | `boolean` | no | Is database enabled? When set to 'disabled', users cannot access the database but Server SDKs with an API key can still read and write to the database. No data is lost when this is toggled. |
