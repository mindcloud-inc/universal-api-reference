# Get Integration with Galileo

Retrieves an integration from Galileo by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/integrations/:name`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Get Integration](https://docs.galileo.ai/api-reference/integrations/get-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Integration name from Galileo, for example openai or anthropic. |
