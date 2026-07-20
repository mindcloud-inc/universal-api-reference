# List Publication Placements with Sponsy

Retrieves publication placements from Sponsy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/publications/:publicationId/placements`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [List Publication Placements](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `list<string>` | yes | Publication to list placements for. |
