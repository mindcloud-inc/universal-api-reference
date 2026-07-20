# Create QR Code with KlipLink

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/qrcodes`
- **Base URL:** `https://api.klipl.ink`
- **Official documentation:** [Create QR Code](https://docs.klipl.ink/api/qrcodes/create-qrcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination_url` | body | `string` | yes | The destination URL the QR code should redirect to. |
| `title` | body | `string` | no | Optional title for the QR code. |
| `description` | body | `string` | no | Optional description for the QR code. |
| `domain` | body | `string` | no | Optional custom domain for the QR code. |
