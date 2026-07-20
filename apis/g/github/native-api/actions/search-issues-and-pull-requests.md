# Search Issues and Pull Requests with GitHub

Finds GitHub issues and pull requests by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/issues`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Search Issues and Pull Requests](https://docs.github.com/en/rest/search/search?apiVersion=2022-11-28#search-issues-and-pull-requests)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Optional free-text GitHub search query. Structured filters are also appended into the final q search string. |
| `advanced_search` | query | `string` | no | Set true to opt into advanced search syntax when needed. |
