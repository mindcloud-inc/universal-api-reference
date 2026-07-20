# Get Form QR Code with Florm

Retrieves a QR code for a Florm form.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/forms/qrcode`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Get Form QR Code](https://api.florm.io/docs#/default/get_qrcode_v1_forms_qrcode_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Public form URL to encode into the QR code image. |
| `download` | query | `boolean` | no | Set true to force a downloadable QR code response. |
