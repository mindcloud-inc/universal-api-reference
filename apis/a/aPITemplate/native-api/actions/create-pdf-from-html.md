# Create PDF From HTML with API Template

Creates a PDF from HTML in API Template.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/create-pdf-from-html`
- **Base URL:** `https://rest.apitemplate.io`
- **Official documentation:** [Create PDF From HTML](https://apitemplate.io/apiv2/#tag/API-Integration/operation/create-pdf-from-html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | HTML body content for the PDF. |
| `css` | body | `string` | no | CSS styles to apply to the PDF. |
| `data` | body | `object` | no | Data values for Jinja placeholders in the HTML body. |
| `settings` | body | `object` | no | Rendering settings for the generated PDF. |
| `export_type` | query | `string` | no | Return the output as JSON metadata or a file response. |
| `expiration` | query | `number` | no | Minutes before the generated file expires; use 0 to store permanently. |
| `output_format` | query | `string` | no | Output format for the generated PDF. |
| `filename` | query | `string` | no | Filename for the generated file. |
| `cloud_storage` | query | `number` | no | Whether to upload the generated file to APITemplate cloud storage. |
| `async` | query | `string` | no | Generate the file asynchronously. |
| `webhook_url` | query | `string` | no | Webhook URL for async completion notifications. |
| `webhook_method` | query | `string` | no | HTTP method for the webhook callback. |
