# Search Issues and Pull Requests with GitHub

Finds GitHub issues and pull requests by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/issues`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Search Issues and Pull Requests](https://docs.github.com/en/rest/search/search?apiVersion=2022-11-28#search-issues-and-pull-requests)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | GitHub search query, for example "is:pr is:open review-requested:@me". Include is:issue or is:pr. |
| `advanced_search` | query | `string` | no | Set true to opt into advanced search syntax when needed. |
| `per_page` | query | `number` | no | The number of results per page (max 100). |
| `sort` | query | `string` | no | Sort field: created, updated or comments. Default is best match. Accepted values: `0`, `1`, `2`. |
| `order` | query | `string` | no | Sort direction: asc or desc. Default is desc. Accepted values: `0`, `1`. |
