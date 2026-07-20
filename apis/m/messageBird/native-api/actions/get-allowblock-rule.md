# Get Allow/Block Rule with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/conversation-allowblock-rules/:allowBlockRuleId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Get Allow/Block Rule](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/get-allow-block-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the allow/block rule. |
| `allowBlockRuleId` | path | `string` | yes | The Bird allow/block rule ID to retrieve. |
