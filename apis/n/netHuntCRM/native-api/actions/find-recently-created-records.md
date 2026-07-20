# Find Recently Created Records with NetHunt CRM

Finds recently created records in NetHunt CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/triggers/new-record/:folderId`
- **Base URL:** `https://nethunt.com/api/v1/zapier`
- **Official documentation:** [Find Recently Created Records](https://nethunt.com/integration-api#new-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID to watch for new records. |
| `since` | query | `string` | no | Only records created after this ISO timestamp are returned. |
