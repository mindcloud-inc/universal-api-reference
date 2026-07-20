# Get Related Content with The Guardian

Retrieves related content for a Guardian item.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{itemPath}}`
- **Base URL:** `https://content.guardianapis.com`
- **Official documentation:** [Get Related Content](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemPath` | path | `string` | yes | Guardian content item path used to resolve related content. |
