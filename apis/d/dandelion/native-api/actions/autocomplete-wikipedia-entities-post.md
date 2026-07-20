# Autocomplete Wikipedia Entities via HTTP POST with Dandelion

Autocompletes Wikipedia entities in Dandelion via HTTP POST.

## Endpoint

- **Method:** `POST`
- **Path:** `/datagraph/wikisearch/v1`
- **Base URL:** `https://api.dandelion.eu`
- **Official documentation:** [Autocomplete Wikipedia Entities via HTTP POST](https://dandelion.eu/docs/api/datagraph/wikisearch/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | Search text to autocomplete against Wikipedia. |
| `lang` | query | `string` | yes | Language of the input text. |
| `limit` | query | `number` | no | Restrict results to the first N matches. |
| `offset` | query | `number` | no | Start listing results from this index. |
| `include` | query | `string` | no | Comma-separated list of extra entity fields to include. |
