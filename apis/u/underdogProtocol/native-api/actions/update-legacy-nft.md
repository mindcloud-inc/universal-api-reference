# Update Legacy NFT with Underdog Protocol

Updates an existing legacy NFT in Underdog Protocol.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/nfts/:mintAddress`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Update Legacy NFT](https://docs.underdogprotocol.com/resources/v1/nfts/update-an-nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mintAddress` | path | `string` | yes | — |
| `description` | body | `string` | no | Description stored in the metadata |
| `image` | body | `string` | yes | Image URL for your NFT |
| `attributes` | body | `object` | no | Key-value pairs of your NFT attributes |
