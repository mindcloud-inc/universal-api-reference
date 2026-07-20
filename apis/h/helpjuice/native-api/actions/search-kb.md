# Search KB with Helpjuice

Finds articles in Helpjuice by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Search KB](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search text to look up in the knowledge base. |
| `category_id` | query | `number` | no | Optional category ID to scope the search. |
