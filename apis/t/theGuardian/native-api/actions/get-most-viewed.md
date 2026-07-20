# Get Most Viewed with The Guardian

Retrieves most-viewed content for a Guardian path.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{itemPath}}`
- **Base URL:** `https://content.guardianapis.com`
- **Official documentation:** [Get Most Viewed](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemPath` | path | `string` | yes | Guardian section, edition, or item path used to resolve most-viewed content. |
