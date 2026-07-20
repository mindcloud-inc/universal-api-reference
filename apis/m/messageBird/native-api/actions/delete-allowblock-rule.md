# Delete Allow/Block Rule with MessageBird

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workspaces/:workspaceId/conversation-allowblock-rules/:allowBlockRuleId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Delete Allow/Block Rule](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/delete-allow-block-rule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the allow/block rule. |
| `allowBlockRuleId` | path | `string` | yes | The Bird allow/block rule ID to delete. |
