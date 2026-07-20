# Get Navigator Coverage with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/navigators/:navigatorId/coverage`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Get Navigator Coverage](https://docs.bird.com/api/channels-api/api-reference/navigators)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the navigator. |
| `navigatorId` | path | `string` | yes | The Bird navigator ID whose coverage should be retrieved. |
