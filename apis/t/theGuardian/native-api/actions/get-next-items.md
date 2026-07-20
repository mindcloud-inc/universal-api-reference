# Get Next Items with The Guardian

Retrieves the next Guardian search results after an item.

## Endpoint

- **Method:** `GET`
- **Path:** `/{{itemPath}}/next`
- **Base URL:** `https://content.guardianapis.com`
- **Official documentation:** [Get Next Items](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/item.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemPath` | path | `string` | yes | Guardian content path or item id, for example sport/2022/oct/07/example-story. |
