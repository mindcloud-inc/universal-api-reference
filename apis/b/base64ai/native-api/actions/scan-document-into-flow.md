# Scan Document into Flow with Base64.ai

Creates a document scan result in a Base64.ai flow.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/scan`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [Scan Document into Flow](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the document to scan into the selected flow. |
| `flowId` | path | `string` | yes | Base64.ai flow ID to attach to the scan request header. |
