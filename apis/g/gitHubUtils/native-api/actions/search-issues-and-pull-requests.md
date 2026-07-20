# Search Issues and Pull Requests with GitHub Utils

Finds issues and pull requests on GitHub by query.

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
| `q` | query | `string` | yes | Search query using GitHub issue and pull request search syntax. |
