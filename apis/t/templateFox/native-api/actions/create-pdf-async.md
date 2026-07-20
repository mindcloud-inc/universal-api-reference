# Create PDF Async with TemplateFox

Creates a PDF generation job in TemplateFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/pdf/create-async`
- **Base URL:** `https://api.templatefox.com`
- **Official documentation:** [Create PDF Async](https://templatefox.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | Template short ID (12 characters). |
| `data` | body | `object` | yes | Template data object. Keys must match template variables. |
| `export_type` | body | `string` | no | Async export type. TemplateFox currently documents only url. |
| `expiration` | body | `number` | no | URL expiration in seconds when export type is url. |
| `filename` | body | `string` | no | Custom filename without the .pdf extension. |
| `store_s3` | body | `boolean` | no | Upload to your configured S3 bucket instead of the CDN. |
| `s3_filepath` | body | `string` | no | Optional path prefix in your S3 bucket. |
| `s3_bucket` | body | `string` | no | Override the default configured S3 bucket. |
| `webhook_url` | body | `string` | no | Public HTTPS URL to receive completion notifications. |
| `webhook_secret` | body | `string` | no | HMAC signing secret for webhook payloads. |
| `pdf_variant` | body | `string` | no | Generate a standards-compliant PDF variant when needed. |
