# Generate Claim Transaction with Underdog Protocol

Creates a claim transaction in Underdog Protocol for an NFT.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/nfts/:mintAddress/claim`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Generate Claim Transaction](https://docs.underdogprotocol.com/resources/nfts/generate-claim-transaction)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mintAddress` | path | `string` | yes |
| `claimerAddress` | body | `string` | no |
| `payerAddress` | body | `string` | no |
| `otp` | body | `string` | no |
