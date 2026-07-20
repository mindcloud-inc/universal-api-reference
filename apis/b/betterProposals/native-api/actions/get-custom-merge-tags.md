# Get Custom Merge Tags with Better Proposals

Retrieves custom merge tags from Better Proposals.

## Endpoint

- **Method:** `GET`
- **Path:** `/settings/merge_tag`
- **Base URL:** `https://api.betterproposals.io`
- **Official documentation:** [Get Custom Merge Tags](https://betterproposals.io/resources/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. Default: 1. |
| `per_page` | query | `number` | no | Results per page. Default: 10. |
