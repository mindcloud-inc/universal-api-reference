# Generate Code Comments with DocuWriter.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate-code-comments`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Generate Code Comments](https://docs.docuwriter.ai/docuwriterai-api-docs/92067)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_code` | body | `string` | yes | Raw source code to comment. |
| `filename` | body | `string` | yes | Name of the source file. |
