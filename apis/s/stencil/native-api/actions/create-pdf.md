# Create PDF with Stencil

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/pdfs`
- **Base URL:** `https://api.usestencil.com`
- **Official documentation:** [Create PDF](https://docs.usestencil.com/api/endpoints/pdfs#create-a-pdf-asynchronously)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata` | body | `object` | no | Extra metadata to include with the result. |
| `modifications[]` | body | `array<object>` | yes | Array of modification objects. |
| `template` | body | `string` | yes | Template ID to generate a PDF from. |
| `webhook_url` | body | `string` | no | Webhook URL called when PDF generation completes. |
