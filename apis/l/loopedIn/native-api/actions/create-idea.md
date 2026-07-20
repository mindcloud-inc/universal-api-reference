# Create Idea with LoopedIn

Creates a new idea in LoopedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/ideas`
- **Base URL:** `https://api.loopedin.io/v1`
- **Official documentation:** [Create Idea](https://docs.loopedin.io/#create-idea)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | The LoopedIn idea category ID. |
| `title` | body | `string` | yes | The idea title. |
| `workspace_id` | body | `string` | yes | The LoopedIn workspace ID. |
