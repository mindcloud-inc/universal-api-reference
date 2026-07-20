# Scan Document Until Page Number with Base64.ai

Creates a Base64.ai scan result up to a specified page number.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/scan`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [Scan Document Until Page Number](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the document to scan with a page limit. |
| `settings` | body | `object` | no | Scan settings object, for example {"limitPages":1}. |
