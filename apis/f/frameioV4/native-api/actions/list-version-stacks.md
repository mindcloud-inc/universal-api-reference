# List Version Stacks with Frame.io v4

Retrieves version stacks from a folder in Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/folders/:folderId/version_stacks`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [List Version Stacks](https://next.developer.frame.io/platform/api-reference/version-stacks/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `include` | query | `string` | no |
