# List Updated Item Details with WeSupply

Retrieves updated item details from WeSupply.

## Endpoint

- **Method:** `GET`
- **Path:** `/external/item-update`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [List Updated Item Details](https://documenter.getpostman.com/view/11859344/T17AiAYq#0d9b38f5-daf9-4cbd-a157-3a58e93cc9b0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EndDate` | query | `string` | no | Inclusive end date for the item update listing window. |
| `ItemStatusId` | query | `string` | no | Optional item status filter for the listing. |
| `Page` | query | `string` | no | Page number for paginated item updates. |
| `Sort` | query | `string` | no | Sort order for the returned item updates. |
| `StartDate` | query | `string` | no | Inclusive start date for the item update listing window. |
