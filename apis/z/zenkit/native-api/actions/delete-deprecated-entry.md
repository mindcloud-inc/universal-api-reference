# Delete Deprecated Entry with Zenkit

Deletes a deprecated item from Zenkit.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/:listAllId/deprecated-entries/:entryAllId`
- **Base URL:** `https://zenkit.com/api/v1`
- **Official documentation:** [Delete Deprecated Entry](https://app.zenkit.com/docs/api/entries/delete-api-v1-lists-listallid-deprecated-entries-entryallid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryAllId` | path | `string` | yes | The entry all id |
| `listAllId` | path | `string` | yes | The list all id |
