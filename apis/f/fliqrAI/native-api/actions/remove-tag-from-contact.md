# Remove Tag From Contact with Fliqr AI

Deletes a tag assignment from a contact in Fliqr AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/:user_id/tags/:tag_id`
- **Base URL:** `https://app.fliqr.ai/api/`
- **Official documentation:** [Remove Tag From Contact](https://docs.fliqr.ai/api-reference/users/delete-users-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | Fliqr contact user ID. |
| `tag_id` | path | `number` | yes | Tag ID to remove. |
