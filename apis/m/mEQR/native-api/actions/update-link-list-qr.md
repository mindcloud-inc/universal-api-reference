# Update Link List QR with ME-QR

Updates a link list QR code in ME-QR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/qr/link-list/update/:entryUID`
- **Base URL:** `https://me-qr.com`
- **Official documentation:** [Update Link List QR](https://me-qr.com/api/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entryUID` | path | `string` | yes | ID or unique entry key for the QR code. |
| `qrFieldsData` | body | `object` | yes | Provider-defined payload object for this QR type. |
