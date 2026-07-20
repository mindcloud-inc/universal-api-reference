# Delete Navigator with MessageBird

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workspaces/:workspaceId/navigators/:navigatorId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Delete Navigator](https://docs.bird.com/api/channels-api/api-reference/navigators)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the navigator. |
| `navigatorId` | path | `string` | yes | The Bird navigator ID to delete. |
