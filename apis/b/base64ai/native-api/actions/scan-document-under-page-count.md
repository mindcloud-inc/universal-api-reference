# Scan Document Under Page Count with Base64.ai

Creates a Base64.ai scan result for documents under a page limit.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/scan`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [Scan Document Under Page Count](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the document to scan with a maximum page count. |
| `settings` | body | `object` | no | Scan settings object, for example {"maxPages":10}. |
