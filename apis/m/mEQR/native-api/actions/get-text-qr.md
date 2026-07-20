# Get Text QR with ME-QR

Retrieves a text QR code from ME-QR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/qr/text/:entryUID`
- **Base URL:** `https://me-qr.com`
- **Official documentation:** [Get Text QR](https://me-qr.com/api/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryUID` | path | `string` | yes | ID or unique entry key for the QR code. |
