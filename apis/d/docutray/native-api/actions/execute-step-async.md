# Start Step Execution with Docutray

## Endpoint

- **Method:** `POST`
- **Path:** `api/steps-async/:stepId`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Start Step Execution](https://docs.docutray.com/docs/operations/steps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_metadata` | body | `object` | no | Optional metadata returned with the step execution result |
| `image_base64` | body | `string` | no | Base64-encoded image or PDF content |
| `image_content_type` | body | `string` | no | Optional MIME type when Docutray cannot infer it |
| `image_url` | body | `string` | no | HTTP or HTTPS URL of the image or PDF to process |
| `stepId` | path | `string` | yes | Step ID for processing |
