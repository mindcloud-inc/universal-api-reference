# Create Form with Optform

Creates a new form in Optform.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Form`
- **Base URL:** `https://optform.azure-api.net`
- **Official documentation:** [Create Form](https://optform.com/help/api/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `workspaceId` | body | `string` | yes |
| `tenantId` | body | `string` | yes |
| `userId` | body | `string` | yes |
