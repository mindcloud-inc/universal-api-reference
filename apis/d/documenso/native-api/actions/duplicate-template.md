# Duplicate Template with Documenso

Creates a duplicate template in Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/template/duplicate`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Duplicate Template](https://docs.documenso.com/docs/developers/api/templates)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templateId` | body | `number` | yes |
