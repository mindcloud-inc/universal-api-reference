# List Tasks with iLovePDFv2

## Endpoint

- **Method:** `GET`
- **Path:** `/task`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [List Tasks](https://www.iloveapi.com/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Task results page. iLoveAPI returns 50 tasks per page. |
| `tool` | query | `string` | no | Optional tool filter. |
| `status` | query | `string` | no | Optional task status filter such as TaskSuccess. |
