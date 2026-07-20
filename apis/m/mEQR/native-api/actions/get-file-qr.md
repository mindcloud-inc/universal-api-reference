# Get File QR with ME-QR

Retrieves a file QR code from ME-QR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/qr/file/:entryUID`
- **Base URL:** `https://me-qr.com`
- **Official documentation:** [Get File QR](https://me-qr.com/api/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryUID` | path | `string` | yes | ID or unique entry key for the QR code. |
