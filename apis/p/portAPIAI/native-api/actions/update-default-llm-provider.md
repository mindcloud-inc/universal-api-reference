# Update Default LLM Provider with Port API AI

Updates the default LLM provider in Port.

## Endpoint

- **Method:** `PUT`
- **Path:** `/llm-providers/defaults`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Default LLM Provider](https://docs.port.io/api-reference/change-default-llm-provider-and-model)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Default model |
| `provider` | body | `string` | yes | Default provider |
