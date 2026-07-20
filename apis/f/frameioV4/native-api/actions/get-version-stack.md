# Get Version Stack with Frame.io v4

Retrieves a version stack from Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/version_stacks/:versionStackId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Get Version Stack](https://next.developer.frame.io/platform/api-reference/version-stacks/show)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `version_stack_id` | path | `string` | yes |
| `include` | query | `string` | no |
