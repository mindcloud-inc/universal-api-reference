# Extract QR Code from Document with Bitskout

Extracts QR code values from a document with Bitskout.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/qrcodes`
- **Base URL:** `https://api.bitskout.com/v2`
- **Official documentation:** [Extract QR Code from Document](https://learn.microsoft.com/en-us/connectors/bitskout/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_url` | body | `string` | no | Direct download URL for the document that contains a QR code. |
