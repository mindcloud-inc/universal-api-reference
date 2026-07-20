# Create QR Code with LinkTwin

Creates a new QR code in LinkTwin.

## Endpoint

- **Method:** `POST`
- **Path:** `/qr/add`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Create QR Code](https://linktw.in/developers#create-a-qr-code)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | body | `string` | yes |
| `data` | body | `string` | yes |
| `background` | body | `string` | no |
| `foreground` | body | `string` | no |
| `logo` | body | `string` | no |
