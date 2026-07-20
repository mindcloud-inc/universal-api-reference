# Get document download URL with Middesk

Retrieves a document download URL from Middesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:id/download_url`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Get document download URL](https://docs.middesk.com/reference/document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the document whose download URL you want to retrieve. |
