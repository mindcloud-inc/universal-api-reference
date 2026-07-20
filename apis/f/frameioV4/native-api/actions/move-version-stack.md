# Move Version Stack with Frame.io v4

Moves a version stack in Frame.io v4.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/version_stacks/:versionStackId/move`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Move Version Stack](https://next.developer.frame.io/platform/api-reference/version-stacks/move)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `version_stack_id` | path | `string` | yes |
| `data` | body | `object` | yes |
