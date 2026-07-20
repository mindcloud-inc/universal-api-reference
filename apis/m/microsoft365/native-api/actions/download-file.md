# Download File with Microsoft 365

Downloads a file from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/drive/items/:itemId/content`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Download File](https://learn.microsoft.com/en-us/graph/api/driveitem-get-content?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | Drive item ID of the file to download. |
