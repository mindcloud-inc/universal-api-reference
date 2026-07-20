# Create QR Code with JmpTo

Creates a QR code in JmpTo.

## Endpoint

- **Method:** `POST`
- **Path:** `/qr/add`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Create QR Code](https://jmpto.net/developers#create-a-qr-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `background` | body | `string` | no | Background RGB color. |
| `foreground` | body | `string` | no | Foreground RGB color. |
| `logo` | body | `string` | no | Path to a PNG or JPG logo. |
| `type` | body | `string` | yes | QR code type: text, vcard, link, email, phone, sms, or wifi. |
| `data` | body | `string` | yes | Data to embed in the QR code. |
