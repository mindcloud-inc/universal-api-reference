# Get Pending Messages with WhatsBoost

Retrieves pending messages from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/get/sms.pending`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Get Pending Messages](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Limit the number of results per page. |
| `page` | body | `number` | no | Pagination of results. |
