# List Recipient Logs with Trolley

Retrieves logs for a recipient from Trolley.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/recipients/:id/logs`
- **Base URL:** `https://api.trolley.com`
- **Official documentation:** [List Recipient Logs](https://developers.trolley.com/api/#retrieve-all-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Recipient ID |
| `page` | query | `string` | no | Page number |
| `pageSize` | query | `string` | no | Page size |
