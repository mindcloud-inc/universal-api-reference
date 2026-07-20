# Get Highlight Lines with LLMWhisperer

Retrieves highlight line metadata from an LLMWhisperer extraction job.

## Endpoint

- **Method:** `GET`
- **Path:** `/highlights`
- **Base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`
- **Official documentation:** [Get Highlight Lines](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_highlighting_api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whisper_hash` | query | `string` | yes | Extraction job hash returned by the extraction API. |
| `lines` | query | `string` | yes | Line range selector such as 1-10. |
