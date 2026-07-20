# List Publication Slots with Sponsy

Retrieves publication slots from Sponsy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/publications/:publicationId/slots`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [List Publication Slots](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `list<string>` | yes | Publication to list slots for. |
