# Search Repositories with GitHub Utils

Finds repositories on GitHub by query.

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
| `q` | query | `string` | yes | Search query using GitHub search syntax. |
