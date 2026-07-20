# List Task Users with Automate Team - Task Management

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1/user_profile`
- **Base URL:** `https://api.automatebusiness.com`
- **Official documentation:** [List Task Users](https://developers.onautomate.com/task)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `string` | yes | PostgREST filter for the workspace id, for example eq.33371. |
| `email` | query | `string` | no | Optional PostgREST filter for email, for example ilike.*@example.com*. |
