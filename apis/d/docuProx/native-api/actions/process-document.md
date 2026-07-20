# Process Document with DocuProx

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/process`
- **Base URL:** `https://api.docuprox.com`
- **Official documentation:** [Process Document](https://docuprox.com/docs/api/#process-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actual_image` | body | `file` | yes | Base64-encoded image or uploaded file to process. |
| `template_id` | body | `string` | yes | UUID of the DocuProx template to use. |
| `static_values` | body | `string` | no | JSON string of static key-value pairs to include in the response. |
