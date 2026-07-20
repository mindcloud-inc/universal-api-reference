# Download Original PDF with Xodo Sign

Retrieves the original PDF from Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/download_raw_document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Download Original PDF](https://eversign.com/api/documentation/methods#download-original-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the document. |
| `document_hash` | query | `string` | yes | The unique document hash to download. |
