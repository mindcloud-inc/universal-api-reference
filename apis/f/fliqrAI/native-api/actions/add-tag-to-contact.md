# Add Tag To Contact with Fliqr AI

Creates a tag assignment for a contact in Fliqr AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:user_id/tags/:tag_id`
- **Base URL:** `https://app.fliqr.ai/api/`
- **Official documentation:** [Add Tag To Contact](https://docs.fliqr.ai/api-reference/users/post-users-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | Fliqr contact user ID. |
| `tag_id` | path | `number` | yes | Tag ID to add. |
