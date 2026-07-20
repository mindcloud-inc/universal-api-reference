# List Schemas with DocuPanda - Document Understanding

Retrieves schemas from DocuPanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/schemas`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [List Schemas](https://docs.docupipe.ai/reference/list_schemas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The maximum number of schemas to return. Maximum is 1000 |
| `offset` | query | `number` | no | The number of schemas to skip (to paginate through the data) |
| `exclude_payload` | query | `boolean` | no | Whether to exclude the jsonSchema payload |
