# Send Thread Message with Cirra

Adds a message to a Cirra thread and starts a run.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/cirra/threads/:threadId/messages`
- **Base URL:** `http://api-public:9801`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threadId` | path | `list` | yes | The thread ID. |
| `content` | body | `string` | yes | The message content to append to the thread. |
