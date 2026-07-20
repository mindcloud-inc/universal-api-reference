# Get Item with The Guardian

Retrieves a Guardian item by path.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{itemPath}}`
- **Base URL:** `https://content.guardianapis.com`
- **Official documentation:** [Get Item](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemPath` | path | `string` | yes | Guardian content path or item id, for example sport/2022/oct/07/example-story. |
| `show-editors-picks` | query | `string` | no | When true, include editors' picks for the requested item path. |
| `show-most-viewed` | query | `string` | no | When true, include most-viewed content for the requested path. |
| `show-related` | query | `string` | no | When true, include related content items. |
| `show-story-package` | query | `string` | no | When true, include story-package content for the requested item. |
