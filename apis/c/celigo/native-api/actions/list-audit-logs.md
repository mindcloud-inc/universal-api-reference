# List Audit Logs with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/audit`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [List Audit Logs](https://developer.celigo.com/api/api-reference/monitoring/audit-logs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceType` | query | `list<string>` | no | Only return entries for this resource type. Accepted values: `accesstoken`, `agent`, `agentgroup`, `alert`, `api`, `ashare`, `asynchelper`, `connection`, `dataset`, `ediprofile`, `environment`, `export`, `file`, `filedefinition`, `flow`, `folder`, `group`, `iclient`, `idpconfig`, `import`, `integration`, `knowledgebase`, `lookupcache`, `mcpserver`, `networkpolicy`, `notification`, `revision`, `role`, `script`, `ssoclient`, `stack`, `supportshare`, `sync`, `tool`, `topic`, `user`. |
| `_resourceId` | query | `string` | no | Only return entries for this resource. Requires Resource Type. |
| `action` | query | `list<string>` | no | Only return entries for this event. Accepted values: `create`, `delete`, `purge`, `purgelogs`, `restore`, `signin`, `signout`, `update`, `view`. |
| `from` | query | `date` | no | Only return entries at or after this time. |
| `to` | query | `date` | no | Only return entries at or before this time. Must not be in the future. |
| `_byUserId` | query | `string` | no | Only return entries by this user ID, or "support" for Celigo support actions. |
| `source` | query | `list<string>` | no | Only return entries from this source. Accepted values: `api`, `cli`, `connector`, `mcp`, `ora`, `script`, `sso`, `stack`, `system`, `ui`. |
| `fieldPath` | query | `string` | no | Restrict field changes to this exact field path. |
