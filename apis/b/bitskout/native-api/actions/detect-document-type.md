# Detect Document Type with Bitskout

Detects a document type with Bitskout.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/doctype_:doctype`
- **Base URL:** `https://api.bitskout.com/v2`
- **Official documentation:** [Detect Document Type](https://learn.microsoft.com/en-us/connectors/bitskout/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doctype` | path | `list<string>` | yes | Document type category to detect. Accepted values: `legal`, `logistics`. |
| `file_url` | body | `string` | no | Direct download URL for the document to classify. |
