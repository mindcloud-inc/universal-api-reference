# Generate Project NFT Claim Link with Underdog Protocol

Retrieves a claim link for a project NFT in Underdog Protocol.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/n/:projectId/nfts/:nftId/claim`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Generate Project NFT Claim Link](https://docs.underdogprotocol.com/resources/projects/nfts/generate-claim-link)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `nftId` | path | `number` | yes |
