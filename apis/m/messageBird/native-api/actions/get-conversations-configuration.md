# Get Conversations Configuration with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/channels/:channelId/conversational`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Get Conversations Configuration](https://docs.bird.com/api/conversations-api/api-reference/channel-configuration/get-conversations-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the channel. |
| `channelId` | path | `string` | yes | The Bird channel ID whose conversations configuration you want to read. |
