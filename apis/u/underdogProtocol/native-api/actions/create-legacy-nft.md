# Create Legacy NFT with Underdog Protocol

Creates a new legacy NFT in Underdog Protocol.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/nfts`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Create Legacy NFT](https://docs.underdogprotocol.com/resources/v1/nfts/create-an-nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for you NFT |
| `description` | body | `string` | no | Description for your NFT |
| `image` | body | `string` | yes | URL pointing to an image for your NFT |
| `attributes` | body | `object` | no | Key-value pairs where the key is the attribute name and the value is the attribute value. |
| `managed` | body | `boolean` | no | Mints the NFT in a Token Manager |
| `upsert` | body | `boolean` | no | Allows updating an NFT if one already exists with the same owner and collection address |
| `ownerAddress` | body | `string` | no | Wallet Address of the owner of the NFT |
| `collectionAddress` | body | `string` | no | Mint address for the NFT Collection |
