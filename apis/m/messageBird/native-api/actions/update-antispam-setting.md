# Update Antispam Setting with MessageBird

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workspaces/:workspaceId/conversations-antispam-settings`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Update Antispam Setting](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/update-antispam-setting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID whose antispam setting should be updated. |
| `enabled` | body | `boolean` | yes | Whether antispam should be enabled for the workspace. |
