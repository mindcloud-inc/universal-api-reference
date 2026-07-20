# Convert Document with Harbour

Converts a Harbour document and returns a download URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:document_id/convert`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [Convert Document](https://developers.harbourshare.com/v2#convert-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | ID of the Harbour document to convert. |
| `format` | query | `string` | no | Target format. Harbour defaults to pdf. |
| `version_number` | query | `number` | no | Specific document version to convert. |
