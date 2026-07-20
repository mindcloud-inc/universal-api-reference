# Generate Code Documentation with DocuWriter.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate-code-documentation`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Generate Code Documentation](https://docs.docuwriter.ai/docuwriterai-api-docs/92064)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_code` | body | `string` | yes | Raw source code to document. |
| `filename` | body | `string` | yes | Name of the source file. |
