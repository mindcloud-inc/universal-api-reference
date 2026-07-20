# Update Webhook Endpoint with LLMWhisperer

Updates an existing webhook endpoint in LLMWhisperer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/whisper-manage-callback`
- **Base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`
- **Official documentation:** [Update Webhook Endpoint](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_webhooks_manage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Updated callback URL to invoke after conversion completes. |
| `auth_token` | body | `string` | yes | Updated bearer token sent by LLMWhisperer when invoking the webhook. |
| `webhook_name` | body | `string` | yes | Existing webhook name to update. |
