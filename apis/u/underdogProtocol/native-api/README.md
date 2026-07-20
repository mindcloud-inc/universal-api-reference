# Underdog Protocol: Native API Reference

A consolidated summary of Underdog Protocol's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.underdogprotocol.com
- **API base URL:** `https://dev.underdogprotocol.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.underdogprotocol.com/guides/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`. The total page count is read from `totalPages`. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Burn Project NFT](actions/burn-project-nft.md) | `POST /v2/projects/n/:projectId/nfts/:nftId/burn` | [docs](https://docs.underdogprotocol.com/resources/projects/nfts/burn-an-nft) |
| [Claim Managed Legacy NFT](actions/claim-managed-legacy-nft.md) | `GET /v1/nfts/:mintAddress/claim` | [docs](https://docs.underdogprotocol.com/resources/v1/managed-nfts/claim) |
| [Create Collection](actions/create-collection.md) | `POST /v1/collections` | [docs](https://docs.underdogprotocol.com/resources/v1/collections/create-a-collection) |
| [Create Legacy NFT](actions/create-legacy-nft.md) | `POST /v1/nfts` | [docs](https://docs.underdogprotocol.com/resources/v1/nfts/create-an-nft) |
| [Create Project](actions/create-project.md) | `POST /v2/projects` | [docs](https://docs.underdogprotocol.com/resources/projects/methods/create-a-project) |
| [Create Project NFT](actions/create-project-nft.md) | `POST /v2/projects/:transferable/:projectId/nfts` | [docs](https://docs.underdogprotocol.com/resources/projects/nfts/create-an-nft) |
| [Create Webhook](actions/create-webhook.md) | `POST /v2/webhooks` | [docs](https://docs.underdogprotocol.com/resources/webhooks/create-a-webhook) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v2/webhooks/:webhookId` | [docs](https://docs.underdogprotocol.com/resources/webhooks/delete-a-webhook) |
| [Generate Claim Transaction](actions/generate-claim-transaction.md) | `POST /v2/nfts/:mintAddress/claim` | [docs](https://docs.underdogprotocol.com/resources/nfts/generate-claim-transaction) |
| [Generate Project NFT Claim Link](actions/generate-project-nft-claim-link.md) | `GET /v2/projects/n/:projectId/nfts/:nftId/claim` | [docs](https://docs.underdogprotocol.com/resources/projects/nfts/generate-claim-link) |
| [Get Collection](actions/get-collection.md) | `GET /v1/collections/:collectionAddress` | [docs](https://docs.underdogprotocol.com/resources/v1/collections/retrieve-a-collection) |
| [Get Legacy NFT](actions/get-legacy-nft.md) | `GET /v1/nfts/:mintAddress` | [docs](https://docs.underdogprotocol.com/resources/v1/nfts/retrieve-an-nft) |
| [Get NFT By Mint Address](actions/get-nft-by-mint-address.md) | `GET /v2/nfts/:mintAddress` | [docs](https://docs.underdogprotocol.com/resources/nfts/retrieve-an-nft) |
| [Get Project](actions/get-project.md) | `GET /v2/projects/:transferable/:projectId` | [docs](https://docs.underdogprotocol.com/resources/projects/methods/retrieve-a-project) |
| [Get Project NFT](actions/get-project-nft.md) | `GET /v2/projects/:transferable/:projectId/nfts/:nftId` | [docs](https://docs.underdogprotocol.com/resources/projects/nfts/retrieve-an-nft) |
| [Get Project Stats](actions/get-project-stats.md) | `GET /v2/projects/:transferable/:projectId/stats` | [docs](https://docs.underdogprotocol.com/resources/projects/methods/retrieve-project-stats) |
| [Get Transaction](actions/get-transaction.md) | `GET /v2/transactions/:transactionId` | [docs](https://docs.underdogprotocol.com/resources/transactions/retrieve-a-transaction) |
| [List Collections](actions/list-collections.md) | `GET /v1/collections` | [docs](https://docs.underdogprotocol.com/resources/v1/collections/list-all-collections) |
| [List Legacy NFTs](actions/list-legacy-nfts.md) | `GET /v1/nfts` | [docs](https://docs.underdogprotocol.com/resources/v1/nfts/list-all-nfts) |
| [List Orgs](actions/list-orgs.md) | `GET /v2/orgs` | [docs](https://docs.underdogprotocol.com/resources/orgs/list-all-orgs) |
| [List Project NFTs](actions/list-project-nfts.md) | `GET /v2/projects/:transferable/:projectId/nfts` | [docs](https://docs.underdogprotocol.com/resources/projects/nfts/list-all-nfts) |
| [List Projects](actions/list-projects.md) | `GET /v2/projects` | [docs](https://docs.underdogprotocol.com/resources/projects/methods/list-all-projects) |
| [List Transactions](actions/list-transactions.md) | `GET /v2/transactions` | [docs](https://docs.underdogprotocol.com/resources/transactions/list-all-transactions) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v2/webhooks` | [docs](https://docs.underdogprotocol.com/resources/webhooks/list-all-webhooks) |
| [Revoke Managed Legacy NFT](actions/revoke-managed-legacy-nft.md) | `GET /v1/nfts/:mintAddress/revoke` | [docs](https://docs.underdogprotocol.com/resources/v1/managed-nfts/revoke) |
| [Revoke Project NFT](actions/revoke-project-nft.md) | `POST /v2/projects/n/:projectId/nfts/:nftId/revoke` | [docs](https://docs.underdogprotocol.com/resources/projects/nfts/revoke-an-nft) |
| [Search Project NFTs](actions/search-project-nfts.md) | `GET /v2/projects/:transferable/:projectId/nfts/search` | [docs](https://docs.underdogprotocol.com/resources/projects/nfts/search-nfts) |
| [Update Legacy NFT](actions/update-legacy-nft.md) | `PUT /v1/nfts/:mintAddress` | [docs](https://docs.underdogprotocol.com/resources/v1/nfts/update-an-nft) |
| [Update Project](actions/update-project.md) | `PUT /v2/projects/:transferable/:projectId` | [docs](https://docs.underdogprotocol.com/resources/projects/methods/update-a-project) |
| [Update Project NFT](actions/update-project-nft.md) | `PUT /v2/projects/:transferable/:projectId/nfts/:nftId` | [docs](https://docs.underdogprotocol.com/resources/projects/nfts/update-an-nft) |
