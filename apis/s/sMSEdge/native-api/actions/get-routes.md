# Get Routes with SMSEdge

Retrieves available routing options from SMSEdge.

## Endpoint

- **Method:** `GET`
- **Path:** `/routes/getall/`
- **Base URL:** `https://api.smsedge.com/v1`
- **Official documentation:** [Get Routes](https://developers.smsedge.io/reference/routes-getall)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_id` | query | `number` | no | ID of specific country. |
| `transactional` | query | `number` | no | Set to 1 to get transactional routes. |
