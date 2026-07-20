# Execute Browser Code with Firecrawl

Executes code in a Firecrawl browser session.

## Endpoint

- **Method:** `POST`
- **Path:** `/browser/:sessionId/execute`
- **Base URL:** `https://api.firecrawl.dev/v2`
- **Official documentation:** [Execute Browser Code](https://docs.firecrawl.dev/api-reference/endpoint/browser-execute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | The browser session ID |
| `code` | body | `string` | yes | Code to execute in the browser sandbox |
| `language` | body | `string` | no | Language of the code to execute |
| `timeout` | body | `number` | no | Execution timeout in seconds |
