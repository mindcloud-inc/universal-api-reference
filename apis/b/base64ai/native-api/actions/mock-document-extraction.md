# Mock Document Extraction with Base64.ai

Creates a mock extraction result in Base64.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/mock/scan`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [Mock Document Extraction](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `string` | yes | Base64-encoded document or image payload for the mock endpoint. |
