# Get Contacts with SMSEdge

Retrieves contact records and details from SMSEdge.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/get/`
- **Base URL:** `https://api.smsedge.com/v1`
- **Official documentation:** [Get Contacts](https://developers.smsedge.io/reference/numbers-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Comma-separated IDs of numbers |
| `limit` | query | `number` | no | Limit of numbers to be returned per request. Max: 1000 |
| `list_id` | query | `number` | no | Numbers from list with this ID will be returned |
| `offset` | query | `number` | no | Subset offset for returned numbers |
