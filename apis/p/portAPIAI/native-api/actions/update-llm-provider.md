# Update LLM Provider with Port API AI

Updates an LLM provider in Port.

## Endpoint

- **Method:** `PUT`
- **Path:** `/llm-providers/:provider`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update LLM Provider](https://docs.port.io/api-reference/change-a-specific-provider-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `boolean` | yes | Provider enabled flag |
| `provider` | path | `string` | yes | The LLM provider identifier. |
