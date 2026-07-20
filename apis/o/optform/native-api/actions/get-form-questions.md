# Get Form Questions with Optform

Retrieves questions for a specific Optform form.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Form/questions/all/:formId`
- **Base URL:** `https://optform.azure-api.net`
- **Official documentation:** [Get Form Questions](https://optform.com/help/api/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `string` | yes |
