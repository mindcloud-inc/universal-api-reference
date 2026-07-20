# List Account Workspaces with Typeform

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/workspaces`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [List Account Workspaces](https://www.typeform.com/developers/create/reference/retrieve-account-workspaces/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Typeform account identifier. |
| `search` | query | `string` | no | Returns items that contain the specified string. |
