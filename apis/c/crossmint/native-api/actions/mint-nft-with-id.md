# Mint NFT with ID with Crossmint

Mints an NFT with an ID in Crossmint.

## Endpoint

- **Method:** `PUT`
- **Path:** `/2022-06-09/collections/:collectionId/nfts/:id`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Mint NFT with ID](https://docs.crossmint.com/api-reference/minting/nfts/mint-nft-idempotent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. Use a real Crossmint collection or credential-template-backed collection ID. |
| `id` | path | `string` | yes | Custom NFT identifier used as the idempotency key. |
| `metadata` | body | `object` | yes | NFT metadata object. Provide at least `name`, `image`, and `description`. |
| `recipient` | body | `string` | yes | Recipient in `<chain>:<address>` or `email:<email_address>:<chain>` format. |
| `sendNotification` | body | `boolean` | no | Notify the recipient by email after minting. Defaults to true. |
| `locale` | body | `string` | no | Locale for notification content. Defaults to `en-US`. |
| `reuploadLinkedFiles` | body | `boolean` | no | Whether metadata URLs should be resolved and reuploaded to IPFS. Defaults to true. |
