# Find Recently Updated Records with NetHunt CRM

Finds recently updated records in NetHunt CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/triggers/updated-record/:folderId`
- **Base URL:** `https://nethunt.com/api/v1/zapier`
- **Official documentation:** [Find Recently Updated Records](https://nethunt.com/integration-api#updated-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldName` | query | `string` | no | Optional field name to limit updates observed. Can be provided more than once. |
| `folderId` | path | `string` | yes | Folder ID to watch for updated records. |
| `since` | query | `string` | no | Only records updated after this ISO timestamp are returned. |
