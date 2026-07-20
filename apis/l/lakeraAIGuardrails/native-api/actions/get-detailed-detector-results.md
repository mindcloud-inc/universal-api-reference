# Get Detailed Detector Results with Lakera AI Guardrails

## Endpoint

- **Method:** `POST`
- **Path:** `/guard/results`
- **Base URL:** `https://api.lakera.ai/v2`
- **Official documentation:** [Get Detailed Detector Results](https://docs.lakera.ai/api-reference/lakera-api/guard-results/get-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Messages comprising the LLM interaction history in OpenAI Chat Completions format. |
| `project_id` | body | `string` | no | Optional Lakera project ID. If omitted, Lakera uses the Guard default policy. |
| `metadata` | body | `object` | no | Optional request metadata such as user or session identifiers. |
| `dev_info` | body | `boolean` | no | Return Lakera Guard build information when true. |
