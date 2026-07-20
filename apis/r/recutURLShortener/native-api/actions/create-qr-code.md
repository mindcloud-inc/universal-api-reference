# Create QR Code with Recut URL Shortener

Creates a QR code in Recut URL Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/qr/add`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Create QR Code](https://app.recut.in/developers#create-a-qr-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `list` | yes | text \| vcard \| link \| email \| phone \| sms \| wifi Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `data` | body | `string` | yes | Data to be embedded inside the QR code |
| `name` | body | `string` | no | QR Code name |
| `background` | body | `string` | no | RGB color such as rgb(255,255,255) |
| `foreground` | body | `string` | no | RGB color such as rgb(0,0,0) |
| `logo` | body | `string` | no | Path to the logo either png or jpg |
