# Get Extraction Details with LLMWhisperer

Retrieves details for an LLMWhisperer extraction job.

## Endpoint

- **Method:** `GET`
- **Path:** `/whisper-detail`
- **Base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`
- **Official documentation:** [Get Extraction Details](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_text_extraction_detail_api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whisper_hash` | query | `string` | yes | Extraction job hash returned by the extraction API. |
