# Get vCard QR with ME-QR

Retrieves a vCard QR code from ME-QR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/qr/vcard/:entryUID`
- **Base URL:** `https://me-qr.com`
- **Official documentation:** [Get vCard QR](https://me-qr.com/api/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryUID` | path | `string` | yes | ID or unique entry key for the QR code. |
