# Get Document with Harbour

Retrieves a specific document from Harbour.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:document_id`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [Get Document](https://developers.harbourshare.com/v2#get-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | ID of the document to retrieve. |
| `version_number` | query | `number` | no | Specific document version to retrieve. Omit to fetch the latest version. |
