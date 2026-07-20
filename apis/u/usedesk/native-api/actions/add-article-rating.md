# Add Article Rating with Usedesk

Adds a rating to a knowledge base article in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/support/:account_id/articles/:id/change-rating`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Add Article Rating](https://api.usedocs.com/article/51402)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Knowledge base ID in the system. |
| `id` | path | `number` | yes | Article ID. |
| `count_positive` | query | `number` | no | Number of positive evaluations to add. |
| `count_negative` | query | `number` | no | Number of negative evaluations to add. |
