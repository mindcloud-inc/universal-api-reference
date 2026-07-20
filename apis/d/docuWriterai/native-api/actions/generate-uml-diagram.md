# Generate UML Diagram with DocuWriter.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate-uml-diagram`
- **Base URL:** `https://app.docuwriter.ai`
- **Official documentation:** [Generate UML Diagram](https://docs.docuwriter.ai/docuwriterai-api-docs/92070)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_code` | body | `string` | yes | Raw source code to analyze. |
| `filename` | body | `string` | yes | Name of the source file. |
| `diagram_type` | body | `string` | yes | Type of UML diagram to generate. |
