# Get Standardization Count with DocuPanda - Document Understanding

Retrieves standardization counts from DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/internal/standardization/count`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Get Standardization Count](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | body | `string` | no | Dataset to filter by |
| `schemaId` | body | `string` | yes | ID of the schema |
