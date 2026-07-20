# List Media with Sendible

## Endpoint

- **Method:** `GET`
- **Path:** `0.2/tw/media`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [List Media](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaLibraryId` | query | `string` | no | Optional media library filter. |
| `name` | query | `string` | no | Optional media name filter. |
| `perPage` | query | `number` | no | Number of media records per page. |
| `status` | query | `string` | no | Comma-separated media statuses to include. |
