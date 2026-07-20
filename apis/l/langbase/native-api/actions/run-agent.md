# Run Agent with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/agent/run`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Run Agent](https://langbase.com/docs/api-reference/agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | LLM model to run the agent with. |
| `input` | body | `string` | yes | Prompt or user input for the agent run. |
| `llmApiKey` | body | `string` | no | Provider LLM API key for the `LB-LLM-Key` request header when the selected model is not already configured in Langbase. |
