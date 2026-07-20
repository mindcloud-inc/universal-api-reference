# Generate PDC QR Code with Qryptal

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api2test.qryptal.com/v2/Vqodes/v2/Vqodes/`
- **Official documentation:** [Generate PDC QR Code](https://dash2.qryptal.com/docs/api2-api/#api-call-generate-qr-pdc)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `string` | yes | JSON string containing the Qryptal payload with data, format, and scheme. |
