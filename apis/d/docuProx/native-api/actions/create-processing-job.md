# Create Processing Job with DocuProx

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/process-job`
- **Base URL:** `https://api.docuprox.com`
- **Official documentation:** [Create Processing Job](https://docuprox.com/docs/api/#process-job-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actual_image` | body | `file` | yes | Base64-encoded image, uploaded file, or ZIP file containing documents. |
| `template_id` | body | `string` | yes | UUID of the DocuProx template to use. |
| `static_values` | body | `string` | no | JSON string of static key-value pairs to include in the job response. |
