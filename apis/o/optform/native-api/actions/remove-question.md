# Remove Question with Optform

Deletes a question from an Optform form.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/Form/:formId/questions/:questionId`
- **Base URL:** `https://optform.azure-api.net`
- **Official documentation:** [Remove Question](https://optform.com/help/api/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `string` | yes |
| `questionId` | path | `string` | yes |
