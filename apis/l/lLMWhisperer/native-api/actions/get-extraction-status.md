# Get Extraction Status with LLMWhisperer

Retrieves the status of an LLMWhisperer extraction job.

## Endpoint

- **Method:** `GET`
- **Path:** `/whisper-status`
- **Base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`
- **Official documentation:** [Get Extraction Status](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_status_api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whisper_hash` | query | `string` | yes | Extraction job hash returned by the extraction API. |
