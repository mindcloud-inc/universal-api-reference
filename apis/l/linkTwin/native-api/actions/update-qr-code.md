# Update QR Code with LinkTwin

Updates an existing QR code in LinkTwin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/qr/:id/update`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Update QR Code](https://linktw.in/developers#update-qr-code)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `type` | body | `string` | yes |
| `data` | body | `string` | yes |
| `background` | body | `string` | no |
| `foreground` | body | `string` | no |
| `logo` | body | `string` | no |
