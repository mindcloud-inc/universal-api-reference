# Send Navigator Message with MessageBird

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/navigators/:navigatorId/messages`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Send Navigator Message](https://docs.bird.com/api/channels-api/api-reference/navigators)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the navigator. |
| `navigatorId` | path | `string` | yes | The Bird navigator ID that should send the message. |
