# Copy Version Stack with Frame.io v4

Copies a version stack in Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/version_stacks/:versionStackId/copy`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Copy Version Stack](https://next.developer.frame.io/platform/api-reference/version-stacks/copy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `version_stack_id` | path | `string` | yes |
| `copy_metadata` | query | `boolean` | no |
| `data` | body | `object` | no |
