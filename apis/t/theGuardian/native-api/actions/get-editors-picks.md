# Get Editors Picks with The Guardian

Retrieves editors' picks for a Guardian path.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{itemPath}}`
- **Base URL:** `https://content.guardianapis.com`
- **Official documentation:** [Get Editors Picks](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemPath` | path | `string` | yes | Guardian section, edition, or item path used to resolve editors' picks. |
