# Create Document From Template with Documenso

Creates a document from a template in Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/template/use`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Create Document From Template](https://docs.documenso.com/docs/developers/api/templates)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templateId` | body | `number` | yes |
| `recipients[]` | body | `array<object>` | yes |
| `distributeDocument` | body | `boolean` | no |
| `externalId` | body | `string` | no |
| `folderId` | body | `string` | no |
| `prefillFields[]` | body | `array<object>` | no |
| `override` | body | `object` | no |
| `formValues` | body | `object` | no |
