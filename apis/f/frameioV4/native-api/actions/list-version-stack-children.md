# List Version Stack Children with Frame.io v4

Retrieves child items for a version stack in Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/version_stacks/:versionStackId/children`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [List Version Stack Children](https://next.developer.frame.io/platform/api-reference/version-stacks/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `version_stack_id` | path | `string` | yes |
| `include` | query | `string` | no |
