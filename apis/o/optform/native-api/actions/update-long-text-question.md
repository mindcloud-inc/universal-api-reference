# Update Long Text Question with Optform

Updates an existing long-text question in an Optform form.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/Form/questions`
- **Base URL:** `https://optform.azure-api.net`
- **Official documentation:** [Update Long Text Question](https://optform.com/help/api/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `sortOrder` | body | `number` | yes |
| `formId` | body | `string` | yes |
| `userId` | body | `string` | yes |
| `title` | body | `string` | yes |
| `question` | body | `string` | yes |
| `content` | body | `string` | yes |
| `_etag` | body | `string` | yes |
