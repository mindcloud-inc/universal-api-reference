# Download Final PDF with Xodo Sign

Retrieves the final PDF from Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/download_final_document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Download Final PDF](https://eversign.com/api/documentation/methods#download-final-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the document. |
| `document_hash` | query | `string` | yes | The unique document hash to download. |
| `audit_trail` | query | `string` | no | Set to 1 to attach the audit trail to the final PDF. |
| `document_id` | query | `string` | no | Optional file selector for multi-file documents or AT for audit trail only. |
| `url_only` | query | `string` | no | Set to 1 to return only the download URL. |
