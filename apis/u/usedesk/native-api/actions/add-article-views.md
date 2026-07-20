# Add Article Views with Usedesk

Adds views to a knowledge base article in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/support/:account_id/articles/:id/add-views`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Add Article Views](https://api.usedocs.com/article/51401)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Knowledge base ID in the system. |
| `id` | path | `number` | yes | Article ID. |
| `count` | query | `number` | no | Number of views to add. |
