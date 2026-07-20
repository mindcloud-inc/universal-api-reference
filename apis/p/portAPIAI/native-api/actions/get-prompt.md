# Get Prompt with Port API AI

Retrieves a prompt from Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp/prompts/:prompt_name`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Prompt](https://docs.port.io/api-reference/get-prompt-by-name)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt_name` | path | `string` | yes | The Port MCP prompt name. |
