# Update Feedback with LoopedIn

Updates an existing feedback item in LoopedIn.

## Endpoint

- **Method:** `PUT`
- **Path:** `/feedback/:id`
- **Base URL:** `https://api.loopedin.io/v1`
- **Official documentation:** [Update Feedback](https://docs.loopedin.io/#feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | The LoopedIn feedback category ID. |
| `id` | path | `string` | yes | The LoopedIn feedback ID. |
| `title` | body | `string` | yes | The updated feedback title. |
