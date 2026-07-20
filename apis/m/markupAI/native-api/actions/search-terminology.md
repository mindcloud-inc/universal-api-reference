# Search Terminology with Markup AI

Finds terminology in Markup AI by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/terminology/search`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Search Terminology](https://docs.markup.ai/api-reference/terminology/search-terminology)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search text for terminology lookup. |
| `domain_ids[]` | query | `array<string>` | no | Optional terminology domain IDs to restrict the search. |
