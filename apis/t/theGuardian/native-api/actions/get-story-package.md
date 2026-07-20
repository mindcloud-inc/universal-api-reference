# Get Story Package with The Guardian

Retrieves story package content for a Guardian item.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{itemPath}}`
- **Base URL:** `https://content.guardianapis.com`
- **Official documentation:** [Get Story Package](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemPath` | path | `string` | yes | Guardian content item path used to resolve story-package content. |
