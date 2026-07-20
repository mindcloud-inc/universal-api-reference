# Create Update with LoopedIn

Creates a new update in LoopedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/updates`
- **Base URL:** `https://api.loopedin.io/v1`
- **Official documentation:** [Create Update](https://docs.loopedin.io/#create-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | The LoopedIn update category ID. |
| `content` | body | `string` | yes | The update content body. |
| `title` | body | `string` | yes | The update title. |
| `workspace_id` | body | `string` | yes | The LoopedIn workspace ID. |
