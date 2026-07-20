# AI Redact Sensitive Information with Nutrient Document Web Services

Updates a document by redacting sensitive information in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai/redact`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [AI Redact Sensitive Information](https://www.nutrient.io/api/reference/public/#tag/AI/operation/ai-redact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documents[]` | body | `array<object>` | yes | Documents to analyze for AI redaction. |
| `criteria` | body | `string` | yes | Natural-language redaction criteria. |
| `redaction_state` | body | `string` | no | Whether to stage or apply the AI redactions. |
| `options` | body | `object` | no | Optional AI redaction configuration. |
| `file` | body | `file` | no | Document file to redact in multipart requests. |
| `data` | body | `object` | no | Multipart request metadata. |
