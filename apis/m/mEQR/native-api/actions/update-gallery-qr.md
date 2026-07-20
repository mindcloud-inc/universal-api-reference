# Update Gallery QR with ME-QR

Updates a gallery QR code in ME-QR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/qr/gallery/update/:entryUID`
- **Base URL:** `https://me-qr.com`
- **Official documentation:** [Update Gallery QR](https://me-qr.com/api/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryUID` | path | `string` | yes | ID or unique entry key for the QR code. |
| `qrFieldsData` | body | `object` | yes | Provider-defined payload object for this QR type. |
