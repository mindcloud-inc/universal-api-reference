# Create PDF with API Template

Creates a PDF in API Template.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/create-pdf`
- **Base URL:** `https://rest.apitemplate.io`
- **Official documentation:** [Create PDF](https://apitemplate.io/apiv2/#tag/API-Integration/operation/create-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | query | `string` | yes | Template ID to render. |
| `export_type` | query | `string` | no | Return the output as JSON metadata or a file response. |
| `expiration` | query | `number` | no | Minutes before the generated file expires; use 0 to store permanently. |
| `output_format` | query | `string` | no | Output format for the generated PDF. |
| `filename` | query | `string` | no | Filename for the generated file. |
| `cloud_storage` | query | `number` | no | Whether to upload the generated file to APITemplate cloud storage. |
| `async` | query | `string` | no | Generate the file asynchronously. |
| `webhook_url` | query | `string` | no | Webhook URL for async completion notifications. |
| `webhook_method` | query | `string` | no | HTTP method for the webhook callback. |
