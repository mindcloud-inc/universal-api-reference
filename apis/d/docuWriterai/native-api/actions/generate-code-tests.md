# Generate Code Tests with DocuWriter.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate-code-tests`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Generate Code Tests](https://docs.docuwriter.ai/docuwriterai-api-docs/92068)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_code` | body | `string` | yes | Raw source code to generate tests for. |
| `filename` | body | `string` | yes | Name of the source file. |
