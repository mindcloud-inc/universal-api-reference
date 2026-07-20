# Get QR code with Appwrite

Retrieves a QR code from Appwrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/avatars/qr`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get QR code](https://appwrite.io/docs/references/cloud/server-rest/avatars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | Plain text to be converted to QR code image. |
| `size` | query | `number` | no | QR code size. Pass an integer between 1 to 1000. Defaults to 400. |
| `margin` | query | `number` | no | Margin from edge. Pass an integer between 0 to 10. Defaults to 1. |
| `download` | query | `boolean` | no | Return resulting image with 'Content-Disposition: attachment ' headers for the browser to start downloading it. Pass 0 for no header, or 1 for otherwise. Default value is set to 0. |
