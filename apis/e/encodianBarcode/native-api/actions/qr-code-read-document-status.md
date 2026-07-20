# QR Code - Read Document Status with Encodian - Barcode

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/Barcodes/GetOperationStatusReadQrCodeFromDocument`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [QR Code - Read Document Status](https://api.apps-encodian.com/swagger/Barcode/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operationId` | query | `string` | yes | Operation ID returned by QR Code - Read from Document. |
