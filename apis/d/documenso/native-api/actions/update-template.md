# Update Template with Documenso

Updates an existing template in Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/template/update`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Update Template](https://docs.documenso.com/docs/developers/api/templates)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templateId` | body | `number` | yes |
| `data` | body | `object` | no |
| `meta` | body | `object` | no |
