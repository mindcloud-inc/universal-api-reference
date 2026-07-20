# Search Documents with Typesense

Finds documents in Typesense by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/{{collection}}/documents/search`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Search Documents](https://typesense.org/docs/30.0/api/search.html#search-parameters)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name. |
