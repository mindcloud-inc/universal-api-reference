# Search Repositories with GitHub

Finds repositories in GitHub by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/repositories`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Search Repositories](https://docs.github.com/en/rest/search/search?apiVersion=2022-11-28#search-repositories)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Optional free-text search terms or prebuilt GitHub qualifiers. Structured filters are also appended into the final `q` search string. |
