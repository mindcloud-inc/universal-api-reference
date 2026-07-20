# Check Plagiarism with Winston AI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/plagiarism`
- **Base URL:** `https://api.gowinston.ai`
- **Official documentation:** [Check Plagiarism](https://docs.gowinston.ai/api-reference/v2/plagiarism/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text to scan for plagiarism. |
| `file` | body | `string` | no | A public PDF, DOC, or DOCX URL to scan instead of raw text. |
| `website` | body | `string` | no | A public website URL to scan instead of raw text. |
| `excluded_sources[]` | body | `array<string>` | no | Domains or URLs to exclude from the plagiarism score. |
| `language` | body | `string` | no | Two-letter language code, or auto for auto-detection. |
| `country` | body | `string` | no | Country code to guide the scan context. |
