# Get Received Messages with WhatsBoost

Retrieves received messages from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/get/sms.received`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Get Received Messages](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Limit the number of results per page. |
| `page` | body | `number` | no | Pagination of results. |
