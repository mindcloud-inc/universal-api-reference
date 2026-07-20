# Ask PDF With AI with XSS PDF Solutions

Creates answers from a PDF in XSS PDF Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/27`
- **Base URL:** `https://api.xss-cross-service-solutions.com/solutions/solutions`
- **Official documentation:** [Ask PDF With AI](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#ask-pdf-with-ai)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The PDF file to be analyzed by AI. |
| `questtext` | body | `string` | yes | The question related to the content of the PDF. |
