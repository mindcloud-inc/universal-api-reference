# Create Publication Slot with Sponsy

Creates a publication slot in Sponsy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/publications/:publicationId/slots`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [Create Publication Slot](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | Publication ID from Sponsy. |
| `date` | body | `string` | yes | Slot date in YYYY-MM-DD format. |
| `status` | body | `string` | yes | Publication status ID. |
| `placement` | body | `string` | yes | Publication placement ID. |
| `content` | body | `string` | yes | Slot ad copy content. |
| `price` | body | `number` | yes | Slot price. |
| `customer` | body | `string` | yes | Customer name. |
| `trackingNumber` | body | `string` | yes | Tracking number for the slot. |
