# Register Webhook Endpoint with LLMWhisperer

Registers a webhook endpoint in LLMWhisperer.

## Endpoint

- **Method:** `POST`
- **Path:** `/whisper-manage-callback`
- **Base URL:** `https://llmwhisperer-api.us-central.unstract.com/api/v2`
- **Official documentation:** [Register Webhook Endpoint](https://docs.unstract.com/llmwhisperer/llm_whisperer/apis/llm_whisperer_webhooks_manage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Callback URL to invoke after conversion completes. |
| `auth_token` | body | `string` | yes | Bearer token sent by LLMWhisperer when invoking the webhook. |
| `webhook_name` | body | `string` | yes | Unique webhook name to register. |
