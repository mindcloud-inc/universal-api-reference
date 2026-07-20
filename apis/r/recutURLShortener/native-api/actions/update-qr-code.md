# Update QR Code with Recut URL Shortener

Updates an existing QR code in Recut URL Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/qr/:id/update`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Update QR Code](https://app.recut.in/developers#update-qr-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | QR code ID |
| `type` | body | `list` | no | text \| vcard \| link \| email \| phone \| sms \| wifi Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `data` | body | `string` | yes | QR code data |
| `background` | body | `string` | no | Background color |
| `foreground` | body | `string` | no | Foreground color |
| `logo` | body | `string` | no | Logo URL |
