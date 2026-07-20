# Update Conversations Configuration with MessageBird

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workspaces/:workspaceId/channels/:channelId/conversational`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Update Conversations Configuration](https://docs.bird.com/api/conversations-api/api-reference/channel-configuration/update-conversations-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the channel configuration. |
| `channelId` | path | `string` | yes | The Bird channel ID whose conversations configuration should be updated. |
