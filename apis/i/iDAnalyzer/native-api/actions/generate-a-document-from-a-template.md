# Generate a document from a template with ID Analyzer

Creates a document from a template in ID Analyzer.

## Endpoint

- **Method:** `POST`
- **Path:** `/generate`
- **Base URL:** `https://api2.idanalyzer.com`
- **Official documentation:** [Generate a document from a template](https://developer.idanalyzer.com/reference/post-generate-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | body | `string` | yes | Output format: PDF, DOCX, or HTML. |
| `templateId` | body | `string` | yes | Stored template ID. |
