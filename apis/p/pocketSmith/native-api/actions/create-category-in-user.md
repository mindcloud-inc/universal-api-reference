# Create Category In User with PocketSmith

Creates a category for a PocketSmith user.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:id/categories`
- **Base URL:** `https://api.pocketsmith.com/v2`
- **Official documentation:** [Create Category In User](https://developers.pocketsmith.com/reference/post_users-id-categories-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `colour` | body | `string` | no | A CSS-style hex colour for the category. |
| `id` | path | `number` | yes | The unique identifier of the PocketSmith user. |
| `title` | body | `string` | yes | A title for the category. |
