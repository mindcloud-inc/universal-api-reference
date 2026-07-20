# Fetch Text Data with Moorcheh

Retrieves text chunks from a Moorcheh namespace with cursor pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `/namespaces/:namespace_name/documents/fetch-text-data`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Fetch Text Data](https://docs.moorcheh.ai/api-reference/data/fetch-text-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace_name` | path | `string` | yes | Name of the text namespace to fetch text chunks from. |
