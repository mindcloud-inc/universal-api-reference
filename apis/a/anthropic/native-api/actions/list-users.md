# List Users with Anthropic

Retrieves users in the Anthropic organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/users`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [List Users](https://platform.claude.com/docs/en/api/admin/users/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before_id` | query | `string` | no | Cursor for previous page. |
| `after_id` | query | `string` | no | Cursor for next page. |
| `limit` | query | `number` | no | Number of records per page. |
| `email` | query | `string` | no | Filter users by email. |
