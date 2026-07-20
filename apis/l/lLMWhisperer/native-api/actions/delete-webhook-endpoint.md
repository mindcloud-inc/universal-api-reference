# Delete Webhook Endpoint with LLMWhisperer

Deletes an existing webhook endpoint from LLMWhisperer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/whisper-manage-callback`
- **Base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`
- **Official documentation:** [Delete Webhook Endpoint](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_webhooks_manage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_name` | query | `string` | yes | Webhook name to delete. |
