# Extract Data From Bytes with Extract Monster

Extracts structured data from file bytes in Extract Monster.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/extract/bytes`
- **Base URL:** `https://api.extract.monster`
- **Official documentation:** [Extract Data From Bytes](https://api.extract.monster/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_bytes` | body | `string` | yes | Base64-encoded file content. |
| `filename` | body | `string` | yes | Original filename with extension. |
