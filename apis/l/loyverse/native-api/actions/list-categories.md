# List Categories with Loyverse

Retrieves category records from the Loyverse catalog.

## Endpoint

- **Method:** `GET`
- **Path:** `/categories`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [List Categories](https://developer.loyverse.com/docs/#tag/Categories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories_ids` | query | `string` | no | Return only categories specified by a comma-separated list of IDs |
| `limit` | query | `number` | no | Used for pagination |
| `cursor` | query | `string` | no | Used for pagination |
| `show_deleted` | query | `boolean` | no | Show deleted modifiers and modifier options |
