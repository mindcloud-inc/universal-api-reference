# Get Received Chats with WhatsBoost

Retrieves received chats from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/get/wa.received`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Get Received Chats](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Limit the number of results per page. |
| `page` | body | `number` | no | Pagination of results. |
