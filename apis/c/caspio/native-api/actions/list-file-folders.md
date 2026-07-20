# List File Folders with Caspio

Retrieves all file folders from Caspio.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/files/folders`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [List File Folders](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Files/ListFilesFolders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalKey` | query | `string` | no | Optional parent folder ID. |
| `pageNumber` | query | `number` | no | Page number. |
| `pageSize` | query | `number` | no | Rows per page. |
| `sortField` | query | `string` | no | Sort field. |
| `sortDescending` | query | `boolean` | no | Set true for descending order. |
