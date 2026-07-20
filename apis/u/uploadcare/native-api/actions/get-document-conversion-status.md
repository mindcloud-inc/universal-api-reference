# Get Document Conversion Status with Uploadcare

Retrieves document conversion status from Uploadcare by token.

## Endpoint

- **Method:** `GET`
- **Path:** `/convert/document/status/:token/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Get Document Conversion Status](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Conversion/operation/documentConvertStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | path | `number` | yes | Conversion job token. |
