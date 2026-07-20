# Delete Address with Bookvault

Deletes an existing address from Bookvault.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/Addresses`
- **Base URL:** `https://api.bookvault.app/v3`
- **Official documentation:** [Delete Address](https://api.bookvault.app/v3/docs#tag/Orders/operation/Addresses_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CommonAddrID` | query | `number` | yes | Bookvault common address ID to delete. |
