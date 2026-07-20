# Search Content with The Guardian

Finds content in The Guardian with optional search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://content.guardianapis.com`
- **Official documentation:** [Search Content](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/content_search.md)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from-date` | query | `string` | no | Return content published on or after this date. |
| `q` | query | `string` | no | Free-text query string used to search Guardian content. |
| `section` | query | `string` | no | Filter results to one or more Guardian sections. |
| `show-blocks` | query | `string` | no | Block expansion mode for each returned item. |
| `show-elements` | query | `string` | no | When true, include element data in each result. |
| `show-fields` | query | `string` | no | Comma-separated content field names to expand in each result. |
| `show-references` | query | `string` | no | Reference expansion mode for each returned item. |
| `show-section` | query | `string` | no | When true, include section information in each result. |
| `show-tags` | query | `string` | no | Tag expansion mode for each returned item. |
| `tag` | query | `string` | no | Filter results to one or more Guardian tags. |
| `to-date` | query | `string` | no | Return content published on or before this date. |
| `use-date` | query | `string` | no | Date field Guardian should use when applying from/to date filters. |
