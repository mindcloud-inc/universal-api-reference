# Generate Multi-File Documentation with DocuWriter.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate-multi-file-documentation`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Generate Multi-File Documentation](https://docs.docuwriter.ai/docuwriterai-api-docs/92069)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files[]` | body | `array<object>` | yes | Array of file objects. |
| `filename` | body | `string` | yes | Name of one source file. |
| `files[].source_code` | body | `string` | yes | Source code for one file. |
