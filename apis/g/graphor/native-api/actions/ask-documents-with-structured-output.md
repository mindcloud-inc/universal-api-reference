# Ask Documents With Structured Output with Graphor

Retrieves structured answers about your documents from Graphor.

## Endpoint

- **Method:** `POST`
- **Path:** `/ask-sources`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Ask Documents With Structured Output](https://docs.graphorlm.com/api-reference/chat-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_ids` | body | `string` | no | Optional list of file IDs to scope the answer to specific documents. |
| `output_schema` | body | `string` | yes | Simplified JSON Schema describing the structured output to return. |
| `question` | body | `string` | yes | The natural-language question to answer with structured output. |
| `thinking_level` | body | `string` | no | Optional thinking level: fast, balanced, or accurate. |
