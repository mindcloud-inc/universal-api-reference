# Extract PDF Content with LLMLayer

Retrieves extracted text from a PDF in LLMLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/get_pdf_content`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Extract PDF Content](https://docs.llmlayer.ai/api-reference/endpoint/scrape-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | PDF URL to process. |
