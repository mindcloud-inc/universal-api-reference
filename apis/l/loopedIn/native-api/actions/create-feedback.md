# Create Feedback with LoopedIn

Creates a new feedback item in LoopedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback`
- **Base URL:** `https://api.loopedin.io/v1`
- **Official documentation:** [Create Feedback](https://docs.loopedin.io/#feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | body | `string` | yes | The LoopedIn feedback board ID. |
| `category` | body | `string` | yes | The LoopedIn feedback category ID. |
| `title` | body | `string` | yes | The feedback title. |
| `workspace_id` | body | `string` | yes | The LoopedIn workspace ID. |
