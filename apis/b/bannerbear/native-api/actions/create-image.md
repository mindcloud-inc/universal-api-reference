# Create Image with Bannerbear

Creates a new image in Bannerbear.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/images`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Create Image](https://developers.bannerbear.com/v2/#create-an-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template` | body | `string` | yes | The Bannerbear image template UID. |
| `modifications` | body | `list<object>` | yes | Layer modifications to apply when generating the image. |
| `webhook_url` | body | `string` | no | Webhook URL to receive the render result. |
| `transparent` | body | `boolean` | no | Render the image with a transparent background when supported. |
| `render_pdf` | body | `boolean` | no | Render a PDF instead of an image when supported. |
| `template_version` | body | `number` | no | Specific template version number to render. |
| `metadata` | body | `string` | no | Custom metadata to attach to the generated image. |
