# Convert Markdown to PDF with Nutrient Document Converter

Converts Markdown to PDF in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/processor/md_to_pdf`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert Markdown to PDF](https://www.nutrient.io/guides/dws-processor/tools-and-api/markdown-to-pdf-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `markdown` | body | `string` | yes | Markdown content to convert into a PDF. |
| `template` | body | `string` | no | Optional built-in template such as built-in:corporate. |
| `css` | body | `string` | no | Optional CSS overrides for the PDF output. |
