# Get Publication Slot with Sponsy

Retrieves a publication slot from Sponsy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/publications/:publicationId/slots/:slotId`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [Get Publication Slot](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | Publication ID from Sponsy. |
| `slotId` | path | `string` | yes | Publication slot ID from Sponsy. |
