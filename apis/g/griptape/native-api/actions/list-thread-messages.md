# List Thread Messages with Griptape

Finds messages in a Griptape thread.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/threads/:thread_id/messages`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [List Thread Messages](https://docs.griptape.ai/stable/griptape-cloud/threads/threads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `thread_id` | path | `string` | yes | The Griptape thread ID whose messages should be listed. |
