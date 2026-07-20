# Get Webhook Details with LLMWhisperer

Retrieves a webhook endpoint from LLMWhisperer by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/whisper-manage-callback`
- **Base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`
- **Official documentation:** [Get Webhook Details](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_webhooks_manage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_name` | query | `string` | yes | Webhook name to retrieve. |
