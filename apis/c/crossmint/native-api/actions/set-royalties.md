# Set Royalties with Crossmint

Updates collection royalties in Crossmint.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1-alpha1/minting/collections/:collectionId/royalties`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Set Royalties](https://docs.crossmint.com/api-reference/minting/collection/set-royalties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. |
| `recipients[0].address` | body | `string` | yes | Royalty recipient address. |
| `recipients[0].basisPoints` | body | `number` | yes | Royalty share in basis points. |
