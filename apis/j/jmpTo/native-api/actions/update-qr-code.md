# Update QR Code with JmpTo

Updates an existing QR code in JmpTo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/qr/:id/update`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Update QR Code](https://jmpto.net/developers#update-qr-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `background` | body | `string` | no | Background RGB color. |
| `foreground` | body | `string` | no | Foreground RGB color. |
| `id` | path | `number` | yes | QR code ID to update. |
| `logo` | body | `string` | no | Path to a PNG or JPG logo. |
| `data` | body | `string` | yes | Data to embed in the QR code. |
