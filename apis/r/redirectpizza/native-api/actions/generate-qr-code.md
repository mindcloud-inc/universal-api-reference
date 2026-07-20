# Generate QR Code with redirect.pizza

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/qr`
- **Base URL:** `https://redirect.pizza`
- **Official documentation:** [Generate QR Code](https://redirect.pizza/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL to encode into the QR code. |
| `format` | query | `string` | no | Output format. redirect.pizza documents png, svg, eps, and json with json as the default. |
