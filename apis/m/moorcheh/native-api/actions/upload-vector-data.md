# Upload Vector Data with Moorcheh

Uploads vector data to a Moorcheh namespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/namespaces/:namespace_name/vectors`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Upload Vector Data](https://docs.moorcheh.ai/api-reference/data/upload-vector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace_name` | path | `string` | yes | Name of the vector namespace to upload vectors to. |
| `vectors[]` | body | `array<object>` | yes | Array of vector objects with id, vector, optional text, and optional metadata fields. |
