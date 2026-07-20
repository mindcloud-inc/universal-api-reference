# Validate QR Code Info Data with Scanova

## Endpoint

- **Method:** `POST`
- **Path:** `/qr/validate-info/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Validate QR Code Info Data](https://docs.scanova.io/api-reference/endpoint/qr_manager/validate-info)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | QR code category ID |
| `info` | body | `string` | yes | QR code info JSON data |
