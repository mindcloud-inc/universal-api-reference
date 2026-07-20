# List Channel Messages with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/channels/:channelId/messages`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [List Channel Messages](https://docs.bird.com/api/channels-api/api-reference/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the channel. |
| `channelId` | path | `string` | yes | The Bird channel ID whose messages should be listed. |
