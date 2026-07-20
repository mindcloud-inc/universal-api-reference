# Get Channel Message with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/channels/:channelId/messages/:messageId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Get Channel Message](https://docs.bird.com/api/channels-api/api-reference/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the channel. |
| `channelId` | path | `string` | yes | The Bird channel ID that owns the message. |
| `messageId` | path | `string` | yes | The Bird message ID to retrieve. |
