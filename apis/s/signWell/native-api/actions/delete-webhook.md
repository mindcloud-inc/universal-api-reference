# Delete Webhook with SignWell

Deletes an existing webhook subscription from SignWell.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/hooks/:id/`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [Delete Webhook](https://developers.signwell.com/reference/delete_api-v1-hooks-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier for a webhook. |
