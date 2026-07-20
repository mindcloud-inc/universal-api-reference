# Get Publication Status with Sponsy

Retrieves a publication status from Sponsy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/publications/:publicationId/status/:statusId`
- **Base URL:** `https://api.getsponsy.com`
- **Official documentation:** [Get Publication Status](https://docs.getsponsy.com/Ad-Inventory-Calendar-10bb55947168808abeb8f73d7a73873e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `list<string>` | yes | Publication ID from List Publications. |
| `statusId` | path | `string` | yes | Status ID from List Publication Statuses. |
