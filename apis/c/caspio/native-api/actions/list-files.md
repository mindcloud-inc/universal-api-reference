# List Files with Caspio

Retrieves all available files from Caspio.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/files`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [List Files](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Files/ListFiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalKey` | query | `string` | no | Optional parent folder ID. |
| `pageNumber` | query | `number` | no | Page number. |
| `pageSize` | query | `number` | no | Rows per page. |
| `sortField` | query | `string` | no | Sort field. |
| `sortDescending` | query | `boolean` | no | Set true for descending order. |
