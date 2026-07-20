# Extract Data From Text with Extract Monster

Extracts structured data from text in Extract Monster.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/extract/text`
- **Base URL:** `https://api.extract.monster`
- **Official documentation:** [Extract Data From Text](https://api.extract.monster/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text content to analyze and extract data from. |
| `schema_form` | body | `string` | no | Optional JSON schema string used to structure the extraction result. |
