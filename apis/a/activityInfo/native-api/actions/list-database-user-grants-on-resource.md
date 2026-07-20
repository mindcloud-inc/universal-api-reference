# List Database User Grants On Resource with ActivityInfo

Retrieves user grants for an ActivityInfo database resource.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/databases/:databaseId/resources/:resourceId/grants`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [List Database User Grants On Resource](https://www.activityinfo.org/support/docs/api/reference/getDatabaseUserGrantsOnResource.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | ActivityInfo database ID. |
| `resourceId` | path | `string` | yes | ActivityInfo database resource ID. |
