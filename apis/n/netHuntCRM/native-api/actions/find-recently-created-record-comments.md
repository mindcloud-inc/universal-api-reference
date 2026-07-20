# Find Recently Created Record Comments with NetHunt CRM

Finds recently created record comments in NetHunt CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/triggers/new-comment/:folderId`
- **Base URL:** `https://nethunt.com/api/v1/zapier`
- **Official documentation:** [Find Recently Created Record Comments](https://nethunt.com/integration-api#new-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID to watch for new comments. |
| `since` | query | `string` | no | Only comments created after this ISO timestamp are returned. |
