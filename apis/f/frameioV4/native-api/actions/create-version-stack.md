# Create Version Stack with Frame.io v4

Creates a new version stack in Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/folders/:folderId/version_stacks`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Create Version Stack](https://next.developer.frame.io/platform/api-reference/version-stacks/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `folder_id` | path | `string` | yes |
| `data` | body | `object` | yes |
