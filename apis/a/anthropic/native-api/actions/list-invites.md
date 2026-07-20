# List Invites with Anthropic

Retrieves invites for the Anthropic organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/invites`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [List Invites](https://platform.claude.com/docs/en/api/admin/invites/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before_id` | query | `string` | no | Cursor for previous page. |
| `after_id` | query | `string` | no | Cursor for next page. |
| `limit` | query | `number` | no | Number of records per page. |
| `email` | query | `string` | no | Filter invites by email. |
| `status` | query | `string` | no | Filter invites by status. |
