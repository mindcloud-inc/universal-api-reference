# Redact Documents with Nutrient Document Web Services

Updates a document with redactions in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/processor/redact`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Redact Documents](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-redact-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | Public PDF URL to redact. |
| `file` | body | `file` | no | PDF file to redact. |
| `strategy` | body | `string` | yes | Redaction strategy to apply. |
| `strategyOptions` | body | `object` | no | Strategy-specific configuration. |
| `redactionState` | body | `string` | no | Whether to stage or apply the redactions. |
| `content[]` | body | `array<object>` | no | Specific content targets to redact. |
| `password` | body | `string` | no | Password for protected PDF files. |
| `data` | body | `object` | no | Multipart request metadata. |
