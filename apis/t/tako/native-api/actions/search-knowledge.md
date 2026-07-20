# Search Knowledge with Tako

Searches Tako Knowledge Cards with natural language.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/knowledge_search`
- **Base URL:** `https://tako.com/api`
- **Official documentation:** [Search Knowledge](https://docs.tako.com/api-reference/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputs.search_effort` | body | `string` | no | Optional search depth. Provider docs describe `fast`, `deep`, and `auto` modes. |
| `inputs.text` | body | `string` | yes | Natural-language query text to send to Tako. |
