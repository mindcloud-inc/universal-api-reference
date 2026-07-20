# Search Company Knowledge with Mona AI

Finds company knowledge in Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/companyKnowledge/searchKnowledge`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Search Company Knowledge](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories[]` | body | `array<string>` | no | Optional knowledge categories to search. |
| `limit` | body | `number` | no | Maximum knowledge results to return. |
| `permission` | body | `string` | yes | Mona permission string required by the knowledge search endpoint. |
| `query` | body | `string` | yes | Knowledge search query. |
| `tags[]` | body | `array<string>` | no | Optional knowledge tags to search. |
