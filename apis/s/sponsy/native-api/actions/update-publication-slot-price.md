# Update Publication Slot Price with Sponsy

Updates a publication slot price in Sponsy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/publications/:publicationId/slots/:slotId`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [Update Publication Slot Price](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | Publication ID from Sponsy. |
| `slotId` | path | `string` | yes | Publication slot ID from Sponsy. |
| `price` | body | `number` | yes | New slot price. |
