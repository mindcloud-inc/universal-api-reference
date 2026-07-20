# Ask Documents with Graphor

Retrieves answers about your documents from Graphor.

## Endpoint

- **Method:** `POST`
- **Path:** `/ask-sources`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Ask Documents](https://docs.graphorlm.com/api-reference/chat-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_ids` | body | `string` | no | Optional list of file IDs to scope the answer to specific documents. |
| `question` | body | `string` | yes | The natural-language question to ask about the ingested documents. |
| `thinking_level` | body | `string` | no | Optional thinking level: fast, balanced, or accurate. |
