# Search Topics with Perigon

Finds topics in Perigon by name or category.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/topics/all`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Search Topics](https://docs.perigon.io/docs/topics)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | query | `string` | no |
| `category` | query | `string` | no |
| `subcategory` | query | `string` | no |
| `page` | query | `number` | no |
| `size` | query | `number` | no |
