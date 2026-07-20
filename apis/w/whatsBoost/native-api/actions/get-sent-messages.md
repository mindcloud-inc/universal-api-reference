# Get Sent Messages with WhatsBoost

Retrieves sent messages from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/get/sms.sent`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Get Sent Messages](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Limit the number of results per page. |
| `page` | body | `number` | no | Pagination of results. |
