# Update Form with Optform

Updates an existing form in Optform.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/Form`
- **Base URL:** `https://optform.azure-api.net`
- **Official documentation:** [Update Form](https://optform.com/help/api/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `name` | body | `string` | yes |
| `workspaceId` | body | `string` | yes |
| `tenantId` | body | `string` | yes |
| `userId` | body | `string` | yes |
| `type` | body | `string` | yes |
| `design` | body | `object` | yes |
| `settings` | body | `object` | yes |
| `share` | body | `object` | yes |
