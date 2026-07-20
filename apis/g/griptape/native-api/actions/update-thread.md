# Update Thread with Griptape

Updates an existing thread in Griptape.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/threads/:thread_id`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Update Thread](https://docs.griptape.ai/stable/griptape-cloud/threads/threads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias` | body | `string` | no | Optional new alias for the thread. |
| `name` | body | `string` | no | Optional new thread name. |
| `thread_id` | path | `string` | yes | The Griptape thread ID to update. |
