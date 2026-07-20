# List Supplies with Ascora

Retrieves supplies from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Inventory/Supplies`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [List Supplies](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=16)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CategoryOneId` | query | `string` | no | Filter by category one ID. |
| `CategoryTwoId` | query | `string` | no | Filter by category two ID. |
| `FavouriteOnly` | query | `boolean` | no | Restrict to favourite supplies only. |
| `FilterText` | query | `string` | no | Search across part number, supplier part number, description, annotation, and category one name. |
