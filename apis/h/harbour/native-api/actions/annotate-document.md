# Annotate Document with Harbour

Adds annotations to an existing document in Harbour.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:document_id/annotate`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [Annotate Document](https://developers.harbourshare.com/v2#annotate-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | ID of the document to annotate. |
| `field_values` | body | `object` | yes | Map of agreementinput-* field identifiers to annotation payloads, for example { "agreementinput-field": { "value": "Example" } }. |
