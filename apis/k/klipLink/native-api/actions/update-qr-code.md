# Update QR Code with KlipLink

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/qrcodes/:short_url`
- **Base URL:** `https://api.klipl.ink`
- **Official documentation:** [Update QR Code](https://docs.klipl.ink/api/qrcodes/update-qrcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `short_url` | path | `string` | yes | The short URL identifier, for example klipl.ink/example. |
| `destination_url` | body | `string` | no | Optional new destination URL for the QR code. |
| `title` | body | `string` | no | Optional new title for the QR code. |
