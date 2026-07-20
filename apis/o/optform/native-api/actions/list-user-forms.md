# List User Forms with Optform

Retrieves forms created by a specific Optform user.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Form/user/:userId`
- **Base URL:** `https://optform.azure-api.net`
- **Official documentation:** [List User Forms](https://optform.com/help/api/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userId` | path | `string` | yes |
