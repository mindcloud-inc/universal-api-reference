# Get Channel Details for a Contact with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/channels/:channelId/contacts/:contactId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Get Channel Details for a Contact](https://docs.bird.com/api/channels-api/api-reference/channels-management)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the channel. |
| `channelId` | path | `string` | yes | The Bird channel ID to inspect. |
| `contactId` | path | `string` | yes | The Bird contact ID to inspect for channel details. |
