# Upload Fax Document with Notifyre SMS

Uploads a fax document to Notifyre.

## Endpoint

- **Method:** `POST`
- **Path:** `/fax/send/conversion`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Upload Fax Document](https://docs.notifyre.com/api/fax-document-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base64Data` | body | `string` | yes | Base64-encoded document contents. |
| `fileName` | body | `string` | yes | Original file name for conversion. |
