# List Shares with Frame.io v4

Retrieves shares for a project in Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/projects/:projectId/shares`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [List Shares](https://next.developer.frame.io/platform/api-reference/shares/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `project_id` | path | `string` | yes |
