# Create Async Task with Cloro

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/async/task`
- **Base URL:** `https://api.cloro.dev`
- **Official documentation:** [Create Async Task](https://docs.cloro.dev/api-reference/endpoint/create-async-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idempotencyKey` | body | `string` | no | Unique string to prevent duplicate task creation. |
| `taskType` | body | `string` | yes | The Cloro AI provider task type to run asynchronously. |
| `webhook.url` | body | `string` | no | Webhook URL for task completion notification. |
| `payload` | body | `object` | yes | Provider-specific request payload. Must include prompt, or query for Google Search. |
| `priority` | body | `number` | no | Task priority from 1 to 10. |
| `webhook` | body | `object` | no | Webhook configuration for task completion notification. |
