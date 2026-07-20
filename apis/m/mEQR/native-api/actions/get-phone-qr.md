# Get Phone QR with ME-QR

Retrieves a phone QR code from ME-QR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/qr/phone/:entryUID`
- **Base URL:** `https://me-qr.com`
- **Official documentation:** [Get Phone QR](https://me-qr.com/api/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryUID` | path | `string` | yes | ID or unique entry key for the QR code. |
