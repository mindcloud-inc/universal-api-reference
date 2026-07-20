# Update Template with Open Letter Connect

Updates a template in Open Letter Connect.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/templates/:id`
- **Base URL:** `https://api.openletterconnect.com/api/v1`
- **Official documentation:** [Update Template](https://api-docs.openletterconnect.com/_templates/update-template/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric template ID from Open Letter Connect. |
| `templatePath` | body | `string` | no | The uploaded template path returned by the upload endpoint. |
| `thumbnailPath` | body | `string` | no | The uploaded thumbnail path returned by the upload endpoint. |
| `title` | body | `string` | no | The updated template title. |
