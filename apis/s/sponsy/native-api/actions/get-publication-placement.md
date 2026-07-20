# Get Publication Placement with Sponsy

Retrieves a publication placement from Sponsy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/publications/:publicationId/placements/:placementId`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [Get Publication Placement](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `list<string>` | yes | Publication ID from List Publications. |
| `placementId` | path | `string` | yes | Placement ID from List Publication Placements. |
