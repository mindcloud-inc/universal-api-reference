# Extract Data From File with Extract Monster

Extracts structured data from a file in Extract Monster.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/extract/file`
- **Base URL:** `https://api.extract.monster`
- **Official documentation:** [Extract Data From File](https://api.extract.monster/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File to upload for structured data extraction. |
| `json_schema` | body | `string` | no | Optional JSON schema string used to structure the extracted output. |
