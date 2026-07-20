# Create Video QR with ME-QR

Creates a video QR code in ME-QR.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/qr/video/create`
- **Base URL:** `https://me-qr.com`
- **Official documentation:** [Create Video QR](https://me-qr.com/api/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `qrFieldsData` | body | `object` | yes | Provider-defined payload object for this QR type. |
