# Delete Feedback with zipBoard

Deletes an existing feedback comment from zipBoard.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/issues/comments/:id`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Delete Feedback](https://help.zipboard.co/article/182-api-for-issues-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Feedback record ID to delete. |
