# Get Gallery QR with ME-QR

Retrieves a gallery QR code from ME-QR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/qr/gallery/:entryUID`
- **Base URL:** `https://me-qr.com`
- **Official documentation:** [Get Gallery QR](https://me-qr.com/api/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryUID` | path | `string` | yes | ID or unique entry key for the QR code. |
