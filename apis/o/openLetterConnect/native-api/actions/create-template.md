# Create Template with Open Letter Connect

Creates a template in Open Letter Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates`
- **Base URL:** `https://api.openletterconnect.com/api/v1`
- **Official documentation:** [Create Template](https://api-docs.openletterconnect.com/_templates/create-template/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[0].defaultValue` | body | `string` | no | The default value for the first template field. |
| `fields[0].key` | body | `string` | no | The merge field token for the first template field. |
| `fields[0].strict` | body | `string` | no | Whether the first template field is strict. |
| `fields[0].value` | body | `string` | no | The display label for the first template field. |
| `productId` | body | `string` | no | The product ID the template belongs to. |
| `templatePath` | body | `string` | no | The uploaded template path returned by the upload endpoint. |
| `thumbnailPath` | body | `string` | no | The uploaded thumbnail path returned by the upload endpoint. |
| `title` | body | `string` | no | The template title. |
