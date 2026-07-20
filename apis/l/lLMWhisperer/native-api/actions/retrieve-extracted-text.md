# Retrieve Extracted Text with LLMWhisperer

Retrieves extracted text from an LLMWhisperer extraction job.

## Endpoint

- **Method:** `GET`
- **Path:** `/whisper-retrieve`
- **Base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`
- **Official documentation:** [Retrieve Extracted Text](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_retrieve_api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whisper_hash` | query | `string` | yes | Extraction job hash returned by the extraction API. |
