# Crossmint: Native API Reference

A consolidated summary of Crossmint's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://docs.crossmint.com/api-reference/introduction
- **API base URL:** `https://staging.crossmint.com/api`

## Authentication

### API Key

Authenticate Crossmint API requests with a server-side API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.crossmint.com/introduction/platform/api-keys/server-side)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Burn NFT](actions/burn-nft.md) | `DELETE /2022-06-09/collections/:collectionId/nfts/:id` | [docs](https://docs.crossmint.com/api-reference/minting/nfts/burn-nft) |
| [Create Collection](actions/create-collection.md) | `POST /2022-06-09/collections` | [docs](https://docs.crossmint.com/api-reference/minting/collection/create-collection) |
| [Create Collection Idempotent](actions/create-collection-idempotent.md) | `PUT /2022-06-09/collections/:collectionId` | [docs](https://docs.crossmint.com/api-reference/minting/collection/create-collection-idempotent) |
| [Create Credential Template](actions/create-credential-template.md) | `POST /v1-alpha1/credentials/templates` | [docs](https://docs.crossmint.com/api-reference/verifiable-credentials/templates/create-template) |
| [Create Credential Type with Name](actions/create-credential-type-with-name.md) | `PUT /v1-alpha1/credentials/types/:typeName` | [docs](https://docs.crossmint.com/api-reference/verifiable-credentials/types/create-named-type) |
| [Create Delegated Signer](actions/create-delegated-signer.md) | `POST /2025-06-09/wallets/:walletLocator/signers` | [docs](https://docs.crossmint.com/api-reference/wallets/register-delegated-key) |
| [Create Order](actions/create-order.md) | `POST /2022-06-09/orders` | [docs](https://docs.crossmint.com/api-reference/headless/create-order) |
| [Create Signature](actions/create-signature.md) | `POST /2025-06-09/wallets/:walletLocator/signatures` | [docs](https://docs.crossmint.com/api-reference/wallets/create-signature) |
| [Create Transaction](actions/create-transaction.md) | `POST /2025-06-09/wallets/:walletLocator/transactions` | [docs](https://docs.crossmint.com/api-reference/wallets/create-transaction) |
| [Create Wallet](actions/create-wallet.md) | `POST /2025-06-09/wallets` | [docs](https://docs.crossmint.com/api-reference/wallets/create-wallet) |
| [Edit NFT](actions/edit-nft.md) | `PATCH /2022-06-09/collections/:collectionId/nfts/:id` | [docs](https://docs.crossmint.com/api-reference/minting/nfts/edit-nft) |
| [Fund Wallet](actions/fund-wallet.md) | `POST /v1-alpha2/wallets/:walletLocator/balances` | [docs](https://docs.crossmint.com/api-reference/wallets/fund-wallet) |
| [Get Action Status](actions/get-action-status.md) | `GET /2022-06-09/actions/:actionId` | [docs](https://docs.crossmint.com/api-reference/common/get-action-status) |
| [Get Collection Info](actions/get-collection-info.md) | `GET /2022-06-09/collections/:collectionId` | [docs](https://docs.crossmint.com/api-reference/minting/collection/get-collection) |
| [Get Credential by Credential ID](actions/get-credential-by-credential-id.md) | `GET /v1-alpha1/credentials/:id` | [docs](https://docs.crossmint.com/api-reference/verifiable-credentials/credentials/retrieve-credential-by-id) |
| [Get Delegated Signer](actions/get-delegated-signer.md) | `GET /2025-06-09/wallets/:walletLocator/signers/:signer` | [docs](https://docs.crossmint.com/api-reference/wallets/get-signer) |
| [Get NFT](actions/get-nft.md) | `GET /2022-06-09/collections/:collectionId/nfts/:id` | [docs](https://docs.crossmint.com/api-reference/minting/nfts/mint-status) |
| [Get Signature](actions/get-signature.md) | `GET /2025-06-09/wallets/:walletLocator/signatures/:signatureId` | [docs](https://docs.crossmint.com/api-reference/wallets/get-signature) |
| [Get Transaction](actions/get-transaction.md) | `GET /2025-06-09/wallets/:walletLocator/transactions/:transactionId` | [docs](https://docs.crossmint.com/api-reference/wallets/get-transaction) |
| [Get Usage](actions/get-usage.md) | `GET /v1-alpha1/projects/:projectId/usage` | [docs](https://docs.crossmint.com/api-reference/admin/get-usage) |
| [Get Wallet Balance](actions/get-wallet-balance.md) | `GET /2025-06-09/wallets/:walletLocator/balances` | [docs](https://docs.crossmint.com/api-reference/wallets/get-wallet-balance) |
| [Get Wallet By Locator](actions/get-wallet-by-locator.md) | `GET /2025-06-09/wallets/:walletLocator` | [docs](https://docs.crossmint.com/api-reference/wallets/get-wallet-by-locator) |
| [Issue Credential](actions/issue-credential.md) | `POST /v1-alpha1/credentials/templates/:templateId/vcs` | [docs](https://docs.crossmint.com/api-reference/verifiable-credentials/credentials/issue-credential) |
| [List Collections](actions/list-collections.md) | `GET /2022-06-09/collections` | [docs](https://docs.crossmint.com/api-reference/minting/collection/get-all-collections) |
| [List NFTs](actions/list-nfts.md) | `GET /2022-06-09/collections/:collectionId/nfts` | [docs](https://docs.crossmint.com/api-reference/minting/nfts/get-nfts) |
| [List NFTs from Wallet](actions/list-nfts-from-wallet.md) | `GET /2022-06-09/wallets/:identifier/nfts` | [docs](https://docs.crossmint.com/api-reference/wallets/get-nfts-from-wallet) |
| [List Signatures](actions/list-signatures.md) | `GET /2025-06-09/wallets/:walletLocator/signatures` | [docs](https://docs.crossmint.com/api-reference/wallets/get-signatures) |
| [List Wallet Transactions](actions/list-wallet-transactions.md) | `GET /2025-06-09/wallets/:walletLocator/transactions` | [docs](https://docs.crossmint.com/api-reference/wallets/get-transactions) |
| [List Wallet Transfers](actions/list-wallet-transfers.md) | `GET /unstable/wallets/:walletLocator/transfers` | [docs](https://docs.crossmint.com/api-reference/wallets/list-transfers) |
| [Mint NFT](actions/mint-nft.md) | `POST /2022-06-09/collections/:collectionId/nfts` | [docs](https://docs.crossmint.com/api-reference/minting/nfts/mint-nft) |
| [Mint NFT with ID](actions/mint-nft-with-id.md) | `PUT /2022-06-09/collections/:collectionId/nfts/:id` | [docs](https://docs.crossmint.com/api-reference/minting/nfts/mint-nft-idempotent) |
| [Mint SFT](actions/mint-sft.md) | `POST /2022-06-09/collections/:collectionId/sfts` | [docs](https://docs.crossmint.com/api-reference/minting/nfts/mint-sft) |
| [Revoke Credential](actions/revoke-credential.md) | `DELETE /v1-alpha1/credentials/:id` | [docs](https://docs.crossmint.com/api-reference/verifiable-credentials/credentials/revoke-credential) |
| [Set Royalties](actions/set-royalties.md) | `PUT /v1-alpha1/minting/collections/:collectionId/royalties` | [docs](https://docs.crossmint.com/api-reference/minting/collection/set-royalties) |
| [Transfer Token](actions/transfer-token.md) | `POST /2025-06-09/wallets/:walletLocator/tokens/:tokenLocator/transfers` | [docs](https://docs.crossmint.com/api-reference/wallets/transfer-token) |
| [Verify Credential](actions/verify-credential.md) | `POST /v1-alpha1/credentials/verification/verify` | [docs](https://docs.crossmint.com/api-reference/verifiable-credentials/credentials/verify-credential) |
