# Create Account Workspace with Typeform

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/workspaces`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Create Account Workspace](https://www.typeform.com/developers/create/reference/create-account-workspace/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Typeform account identifier. |
| `name` | body | `string` | no | Name of the new workspace. |
