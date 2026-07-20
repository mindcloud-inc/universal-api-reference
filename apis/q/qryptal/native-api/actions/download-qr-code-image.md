# Download QR Code Image with Qryptal

## Endpoint

- **Method:** `GET`
- **Path:** `:uid/qr:uid.png`
- **Base URL:** `https://api2test.qryptal.com/v2/Vqodes/v2/Vqodes/`
- **Official documentation:** [Download QR Code Image](https://dash2.qryptal.com/docs/api2-api/#created-qr-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | Unique Qryptal identifier returned when the QR code was created. |
| `code_token` | query | `string` | yes | The code_token value returned by QR creation. |
| `bg` | query | `number` | no | Set to 0 to request a transparent background. |
| `s` | query | `number` | no | Optional image size selector documented by Qryptal. |
