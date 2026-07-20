# List Items with Webflow

Retrieves staged collection items from Webflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/:collection_id/items`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [List Items](https://developers.webflow.com/data/reference/cms/collection-items/staged-items/list-items)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | The unique identifier of the collection. |
| `offset` | query | `number` | no | Number of items to skip before returning results. |
| `limit` | query | `number` | no | Maximum number of items to return. |
| `name` | query | `string` | no | Optional name selector for returned items. |
| `slug` | query | `string` | no | Optional slug selector for returned items. |
| `sortBy` | query | `string` | no | Field used to sort returned items. |
| `sortOrder` | query | `string` | no | Sort direction for returned items. |
