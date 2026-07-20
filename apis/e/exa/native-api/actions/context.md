# Context with Exa

Retrieves context from Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/context`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Context](https://exa.ai/docs/reference/context)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search query to find relevant code context. |
| `tokensNum` | body | `number` | no | Token budget for the response. Use a number or dynamic. |
