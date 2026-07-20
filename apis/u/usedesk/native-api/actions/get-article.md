# Get Article with Usedesk

Retrieves a knowledge base article by ID from Usedesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/support/:account_id/articles/:id`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Get Article](https://api.usedocs.com/article/51400)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Knowledge base ID in the system. |
| `id` | path | `number` | yes | Article ID. |
