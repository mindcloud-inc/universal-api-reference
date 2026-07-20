# Get Email QR with ME-QR

Retrieves an email QR code from ME-QR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/qr/email/:entryUID`
- **Base URL:** `https://me-qr.com`
- **Official documentation:** [Get Email QR](https://me-qr.com/api/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryUID` | path | `string` | yes | ID or unique entry key for the QR code. |
