# Delete Records with AITable.ai

Deletes existing records from a datasheet in AITable.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/fusion/v1/datasheets/:datasheetId/records`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Delete Records](https://developers.aitable.ai/api/reference/#delete-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasheetId` | path | `string` | yes | AITable datasheet ID containing records to delete. |
| `recordIds` | query | `string<string>` | yes | One or more AITable record IDs to delete. |
