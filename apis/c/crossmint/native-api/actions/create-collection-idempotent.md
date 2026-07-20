# Create Collection Idempotent with Crossmint

Creates a collection idempotently in Crossmint.

## Endpoint

- **Method:** `PUT`
- **Path:** `/2022-06-09/collections/:collectionId`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Create Collection Idempotent](https://docs.crossmint.com/api-reference/minting/collection/create-collection-idempotent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Custom collection identifier. |
| `chain` | body | `string` | yes | Blockchain for the collection. |
| `metadata.name` | body | `string` | yes | Collection display name. |
| `metadata.description` | body | `string` | yes | Collection description. |
| `metadata.imageUrl` | body | `string` | yes | Collection image URL. |
| `metadata.symbol` | body | `string` | yes | Collection symbol. |
