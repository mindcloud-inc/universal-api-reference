# Get Pending Chats with WhatsBoost

Retrieves pending chats from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/get/wa.pending`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Get Pending Chats](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Limit the number of results per page. |
| `page` | body | `number` | no | Pagination of results. |
