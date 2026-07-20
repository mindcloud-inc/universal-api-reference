# Get Content By IDs with The Guardian

Retrieves Guardian content items by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://content.guardianapis.com`
- **Official documentation:** [Get Content By IDs](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/content_search.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | Comma-separated Guardian content ids to fetch exactly. |
| `show-fields` | query | `string` | no | Comma-separated content field names to expand in each matched item. |
