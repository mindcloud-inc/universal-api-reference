# Check Facts with Winston AI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/fact-checker`
- **Base URL:** `https://api.gowinston.ai`
- **Official documentation:** [Check Facts](https://docs.gowinston.ai/api-reference/v2/fact-checker/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text to fact-check. |
| `file` | body | `string` | no | A public PDF, DOC, or DOCX URL to fact-check instead of raw text. |
| `website` | body | `string` | no | A public website URL to fact-check instead of raw text. |
| `language` | body | `string` | no | Two-letter language code, or auto for auto-detection. |
