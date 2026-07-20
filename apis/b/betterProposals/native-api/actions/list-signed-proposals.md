# List Signed Proposals with Better Proposals

Retrieves signed proposals from Better Proposals.

## Endpoint

- **Method:** `GET`
- **Path:** `/proposal/signed`
- **Base URL:** `https://api.betterproposals.io`
- **Official documentation:** [List Signed Proposals](https://betterproposals.io/resources/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. Default: 1. |
| `per_page` | query | `number` | no | Results per page. Default: 10. |
| `type` | query | `string` | no | DocumentTypeID for filtering. |
