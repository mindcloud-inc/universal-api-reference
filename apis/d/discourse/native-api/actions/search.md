# Search with Discourse

Finds Discourse content by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/search.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Search](https://docs.discourse.org/#tag/Search/operation/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `string` | no | Search results page number. |
| `q` | query | `string` | yes | Search query string using Discourse search syntax. |
