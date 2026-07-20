# Convert Document From Base64 with Harbour

Converts a base64 document in Harbour and returns a download URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/convert`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [Convert Document From Base64](https://developers.harbourshare.com/v2#convert-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_base64` | body | `string` | yes | Base64 string for the source document file. |
| `filename` | body | `string` | yes | Original filename including extension. |
| `final_format` | body | `string` | no | Requested output format. Harbour defaults to pdf. |
