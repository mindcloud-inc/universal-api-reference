# Find Records with NetHunt CRM

Finds records in NetHunt CRM by ID or query.

## Endpoint

- **Method:** `GET`
- **Path:** `/searches/find-record/:folderId`
- **Base URL:** `https://nethunt.com/api/v1/zapier`
- **Official documentation:** [Find Records](https://nethunt.com/integration-api#find-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID to search within. |
| `query` | query | `string` | no | Advanced search query used to find records when Record ID is not provided. |
| `recordId` | query | `string` | no | Record ID if you already know the exact record. |
