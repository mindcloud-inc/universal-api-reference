# <img src="https://images.mindcloud.co/apps/icons/crossmint_1775062463098.png" alt="Crossmint logo" width="28" height="28"> Crossmint: Universal API

Create wallets, move stablecoins, and tokenize digital assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/crossmint/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.crossmint.com/
- **Vendor API docs:** https://docs.crossmint.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-usage?connectionId=$CONNECTION_ID&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Action Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Status](actions/get-action-status.md) | GET | Retrieves action status from Crossmint. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a collection in Crossmint. |
| [Create Collection Idempotent](actions/create-collection-idempotent.md) | POST | Creates a collection idempotently in Crossmint. |
| [Get Collection Info](actions/get-collection-info.md) | GET | Retrieves collection information from Crossmint. |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from Crossmint. |

### Collection Royalties

| Action | Method | Description |
| --- | --- | --- |
| [Set Royalties](actions/set-royalties.md) | PUT | Updates collection royalties in Crossmint. |

### Credential

| Action | Method | Description |
| --- | --- | --- |
| [Get Credential by Credential ID](actions/get-credential-by-credential-id.md) | GET | Retrieves a credential from Crossmint by credential ID. |
| [Issue Credential](actions/issue-credential.md) | POST | Issues a credential in Crossmint. |
| [Revoke Credential](actions/revoke-credential.md) | DELETE | Revokes a credential in Crossmint. |

### Credential Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Credential Template](actions/create-credential-template.md) | POST | Creates a credential template in Crossmint. |

### Credential Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Credential Type with Name](actions/create-credential-type-with-name.md) | POST | Creates a credential type with a name in Crossmint. |

### Credential Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Credential](actions/verify-credential.md) | GET | Verifies a credential in Crossmint. |

### Delegated Signer

| Action | Method | Description |
| --- | --- | --- |
| [Create Delegated Signer](actions/create-delegated-signer.md) | POST | Creates a delegated signer in Crossmint. |
| [Get Delegated Signer](actions/get-delegated-signer.md) | GET | Retrieves a delegated signer from Crossmint. |

### Nft

| Action | Method | Description |
| --- | --- | --- |
| [Burn NFT](actions/burn-nft.md) | DELETE | Burns an NFT from Crossmint. |
| [Edit NFT](actions/edit-nft.md) | PUT | Updates NFT metadata in Crossmint. |
| [Get NFT](actions/get-nft.md) | GET | Retrieves NFT status from Crossmint. |
| [List NFTs](actions/list-nfts.md) | GET | Retrieves NFTs from a Crossmint collection. |
| [List NFTs from Wallet](actions/list-nfts-from-wallet.md) | GET | Retrieves NFTs from a Crossmint wallet. |
| [Mint NFT](actions/mint-nft.md) | POST | Mints an NFT in Crossmint. |
| [Mint NFT with ID](actions/mint-nft-with-id.md) | POST | Mints an NFT with an ID in Crossmint. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates an order in Crossmint. |

### Project Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves project usage data from Crossmint. |

### Sft

| Action | Method | Description |
| --- | --- | --- |
| [Mint SFT](actions/mint-sft.md) | POST | Mints an SFT in Crossmint. |

### Signature

| Action | Method | Description |
| --- | --- | --- |
| [Create Signature](actions/create-signature.md) | POST | Creates a signature in Crossmint. |
| [Get Signature](actions/get-signature.md) | GET | Retrieves a signature from Crossmint. |
| [List Signatures](actions/list-signatures.md) | GET | Retrieves signatures from Crossmint. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST | Creates a transaction in Crossmint. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Crossmint. |
| [List Wallet Transactions](actions/list-wallet-transactions.md) | GET | Retrieves wallet transactions from Crossmint. |

### Transfer

| Action | Method | Description |
| --- | --- | --- |
| [List Wallet Transfers](actions/list-wallet-transfers.md) | GET | Retrieves wallet transfer activity from Crossmint. |
| [Transfer Token](actions/transfer-token.md) | POST | Transfers a token from a Crossmint wallet. |

### Wallet

| Action | Method | Description |
| --- | --- | --- |
| [Create Wallet](actions/create-wallet.md) | POST | Creates a new wallet in Crossmint. |
| [Get Wallet By Locator](actions/get-wallet-by-locator.md) | GET | Retrieves a wallet from Crossmint by locator. |

### Wallet Balance

| Action | Method | Description |
| --- | --- | --- |
| [Fund Wallet](actions/fund-wallet.md) | POST | Funds a wallet in Crossmint. |
| [Get Wallet Balance](actions/get-wallet-balance.md) | GET | Retrieves a wallet balance from Crossmint. |

