# Scan Document with Document Types with Base64.ai

Creates a Base64.ai scan result using specified document types.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/scan`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [Scan Document with Document Types](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the document to scan with constrained document types. |
| `modelTypes[]` | body | `array<string>` | yes | Document model type identifiers to constrain classification. |
