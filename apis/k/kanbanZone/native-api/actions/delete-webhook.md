# Delete Webhook with Kanban Zone

Deletes an existing webhook from Kanban Zone.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://integrations.kanbanzone.io/v1`
- **Official documentation:** [Delete Webhook](https://docs.kanbanzone.io/apiReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the webhook to delete |
