# List Templates with Better Proposals

Retrieves all templates from Better Proposals.

## Endpoint

- **Method:** `GET`
- **Path:** `/template`
- **Base URL:** `https://api.betterproposals.io`
- **Official documentation:** [List Templates](https://betterproposals.io/resources/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. Default: 1. |
| `per_page` | query | `number` | no | Results per page. Default: 10. |
