# List Cards with Fidel API

Retrieves cards from a Fidel program.

## Endpoint

- **Method:** `GET`
- **Path:** `/programs/:programId/cards`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [List Cards](https://reference.fidel.uk/reference/list-cards)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `programId` | path | `string` | yes |
