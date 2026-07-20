# Natural Language Search Documents with Typesense

Finds documents in Typesense using natural language search.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/{{collection}}/documents/search`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Natural Language Search Documents](https://typesense.org/docs/30.0/api/natural-language-search.html)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name. |
| `nl_query` | query | `string` | yes | Natural language search query. |
| `query_by` | query | `string` | yes | Fields to search. |
