# Create Image Synchronously with Stencil

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/sync`
- **Base URL:** `https://api.usestencil.com`
- **Official documentation:** [Create Image Synchronously](https://docs.usestencil.com/api/endpoints/image#create-image-synchronously)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jpeg_quality` | body | `number` | no | JPEG quality between 0 and 1. |
| `metadata` | body | `object` | no | Extra metadata to include with the result. |
| `modifications[]` | body | `array<object>` | no | Array of modification objects. |
| `png_multiplier` | body | `number` | no | PNG quality multiplier. |
| `template` | body | `string` | no | Template ID to generate from. |
| `transparent` | body | `boolean` | no | Whether the generated image background should be transparent. |
| `webhook_url` | body | `string` | no | Webhook URL called when image processing completes. |
