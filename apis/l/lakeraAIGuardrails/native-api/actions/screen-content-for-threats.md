# Screen Content for Threats with Lakera AI Guardrails

## Endpoint

- **Method:** `POST`
- **Path:** `/guard`
- **Base URL:** `https://api.lakera.ai/v2`
- **Official documentation:** [Screen Content for Threats](https://docs.lakera.ai/api-reference/lakera-api/guard/screen-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Messages comprising the LLM interaction history in OpenAI Chat Completions format. |
| `project_id` | body | `string` | no | Optional Lakera project ID. If omitted, Lakera uses the Guard default policy. |
| `payload` | body | `boolean` | no | Return detected PII, profanity, or custom regex match locations when available. |
| `breakdown` | body | `boolean` | no | Return the detector breakdown used for the flagging decision. |
| `metadata` | body | `object` | no | Optional request metadata such as user or session identifiers. |
| `dev_info` | body | `boolean` | no | Return Lakera Guard build information when true. |
