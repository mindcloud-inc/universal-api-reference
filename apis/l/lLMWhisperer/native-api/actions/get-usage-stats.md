# Get Usage Stats with LLMWhisperer

Retrieves tagged usage statistics from LLMWhisperer.

## Endpoint

- **Method:** `GET`
- **Path:** `/usage`
- **Base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`
- **Official documentation:** [Get Usage Stats](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_usage_stats/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | query | `string` | yes | Tag to filter usage statistics. |
| `from_date` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `to_date` | query | `date` | no | End date in YYYY-MM-DD format. |
