# List Workspaces with Frame.io v4

Retrieves workspaces from an account in Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/workspaces`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [List Workspaces](https://next.developer.frame.io/platform/api-reference/workspaces/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `include` | query | `string` | no |
