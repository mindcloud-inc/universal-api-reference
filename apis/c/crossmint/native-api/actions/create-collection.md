# Create Collection with Crossmint

Creates a collection in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/2022-06-09/collections`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Create Collection](https://docs.crossmint.com/api-reference/minting/collection/create-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | body | `string` | yes | Blockchain for the collection. |
| `metadata.name` | body | `string` | yes | Collection display name. |
| `metadata.description` | body | `string` | yes | Collection description. |
| `metadata.imageUrl` | body | `string` | yes | Collection image URL. |
| `metadata.symbol` | body | `string` | yes | Collection symbol. |
| `fungibility` | body | `string` | yes | Collection fungibility. |
| `transferable` | body | `boolean` | no | Whether NFTs are transferable. |
| `supplyLimit` | body | `number` | no | Maximum supply for the collection. |
| `payments.price` | body | `string` | no | Mint price for the collection. |
| `payments.recipientAddress` | body | `string` | no | Address that receives collection payments. |
| `payments.currency` | body | `string` | no | Currency for collection payments. |
| `reuploadLinkedFiles` | body | `boolean` | no | Whether metadata URLs are reuploaded to IPFS. |
