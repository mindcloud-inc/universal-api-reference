# Update Feedback with zipBoard

Updates an existing feedback comment in zipBoard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/issues/comments/:id`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Update Feedback](https://help.zipboard.co/article/182-api-for-issues-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated feedback description. |
| `id` | path | `string` | yes | Feedback record ID to update. |
| `title` | body | `string` | yes | Updated feedback title. |
