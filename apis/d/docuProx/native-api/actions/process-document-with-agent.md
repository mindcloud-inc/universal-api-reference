# Process Document with Agent with DocuProx

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/process-agent`
- **Base URL:** `https://api.docuprox.com`
- **Official documentation:** [Process Document with Agent](https://docuprox.com/docs/api/#process-agent-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actual_image` | body | `string` | yes | Base64-encoded image or uploaded file to process. |
| `template_id` | body | `string` | no | UUID of the DocuProx template to use. |
| `payload` | body | `object` | yes | JSON payload with document type, prompt configuration, and optional static values. |
