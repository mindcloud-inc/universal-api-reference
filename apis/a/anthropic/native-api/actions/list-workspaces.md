# List Workspaces with Anthropic

Retrieves workspaces in the Anthropic organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/workspaces`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [List Workspaces](https://platform.claude.com/docs/en/api/admin/workspaces/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before_id` | query | `string` | no | Cursor for previous page. |
| `after_id` | query | `string` | no | Cursor for next page. |
| `limit` | query | `number` | no | Number of records per page. |
| `include_archived` | query | `boolean` | no | Whether to include archived workspaces. |
