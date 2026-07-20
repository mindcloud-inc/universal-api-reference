# Find Recent Record Changes with NetHunt CRM

Finds recent record changes in NetHunt CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/triggers/record-change/:folderId`
- **Base URL:** `https://nethunt.com/api/v1/zapier`
- **Official documentation:** [Find Recent Record Changes](https://nethunt.com/integration-api#record-change)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldName` | query | `string` | no | Optional field name to limit changes observed. Can be provided more than once. |
| `folderId` | path | `string` | yes | Folder ID to inspect for record changes. |
| `recordId` | query | `string` | no | Optional record ID to limit the result to a single record. |
| `since` | query | `string` | no | Only changes made after this ISO timestamp are returned. |
