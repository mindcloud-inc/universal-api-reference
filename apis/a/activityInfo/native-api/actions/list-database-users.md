# List Database Users with ActivityInfo

Retrieves users for a specific ActivityInfo database.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/databases/:databaseId/users`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [List Database Users](https://www.activityinfo.org/support/docs/api/reference/getDatabaseUsers.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | ActivityInfo database ID. |
