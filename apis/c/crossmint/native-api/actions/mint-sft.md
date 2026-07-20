# Mint SFT with Crossmint

Mints an SFT in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/2022-06-09/collections/:collectionId/sfts`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Mint SFT](https://docs.crossmint.com/api-reference/minting/nfts/mint-sft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection identifier. |
| `templateId` | body | `string` | yes | SFT template identifier. |
| `recipient` | body | `string` | yes | Recipient address. |
| `sendNotification` | body | `boolean` | no | Email notification flag. |
| `locale` | body | `string` | no | Locale for notification content. |
| `amount` | body | `number` | no | Amount to mint. |
