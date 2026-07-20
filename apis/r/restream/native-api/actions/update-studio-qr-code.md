# Update Studio QR Code with Restream

Updates a studio QR code in Restream.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/user/studio/qr-codes/:qrCodeId`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [Update Studio QR Code](https://developers.restream.io/studio/studio-qr-code-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `link` | body | `string` | no | Updated QR code destination link. |
| `qrCodeId` | path | `string` | yes | The ID of the QR code to update. |
| `title` | body | `string` | no | Updated QR code title. |
