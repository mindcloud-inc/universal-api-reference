# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-06-as-20_1775517518839.png" alt="Underdog Protocol logo" width="28" height="28"> Underdog Protocol: Universal API

Mint NFTs and manage projects, collections, transactions, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/underdogProtocol/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://underdogprotocol.com
- **Vendor API docs:** https://docs.underdogprotocol.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Burn Project NFT](actions/burn-project-nft.md) | DELETE | Burns a project NFT in Underdog Protocol. |
| [Claim Managed Legacy NFT](actions/claim-managed-legacy-nft.md) | GET | Retrieves claim data for a managed legacy NFT in Underdog Protocol. |
| [Create Legacy NFT](actions/create-legacy-nft.md) | POST | Creates a new legacy NFT in Underdog Protocol. |
| [Create Project NFT](actions/create-project-nft.md) | POST | Creates a new project NFT in Underdog Protocol. |
| [Generate Project NFT Claim Link](actions/generate-project-nft-claim-link.md) | GET | Retrieves a claim link for a project NFT in Underdog Protocol. |
| [Get Legacy NFT](actions/get-legacy-nft.md) | GET | Retrieves a legacy NFT from Underdog Protocol. |
| [Get NFT By Mint Address](actions/get-nft-by-mint-address.md) | GET | Retrieves an NFT from Underdog Protocol by mint address. |
| [Get Project NFT](actions/get-project-nft.md) | GET | Retrieves a project NFT from Underdog Protocol. |
| [List Legacy NFTs](actions/list-legacy-nfts.md) | GET | Retrieves a list of legacy NFTs from Underdog Protocol. |
| [List Project NFTs](actions/list-project-nfts.md) | GET | Retrieves NFTs from a project in Underdog Protocol. |
| [Revoke Managed Legacy NFT](actions/revoke-managed-legacy-nft.md) | PUT | Revokes a managed legacy NFT in Underdog Protocol. |
| [Revoke Project NFT](actions/revoke-project-nft.md) | PUT | Revokes a project NFT in Underdog Protocol. |
| [Search Project NFTs](actions/search-project-nfts.md) | GET | Finds project NFTs in Underdog Protocol by search term. |
| [Update Legacy NFT](actions/update-legacy-nft.md) | PUT | Updates an existing legacy NFT in Underdog Protocol. |
| [Update Project NFT](actions/update-project-nft.md) | PUT | Updates an existing project NFT in Underdog Protocol. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Underdog Protocol. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection from Underdog Protocol. |
| [List Collections](actions/list-collections.md) | GET | Retrieves a list of collections from Underdog Protocol. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Orgs](actions/list-orgs.md) | GET | Retrieves a list of organizations from Underdog Protocol. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Underdog Protocol. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Underdog Protocol. |
| [Get Project Stats](actions/get-project-stats.md) | GET | Retrieves project stats from Underdog Protocol. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Underdog Protocol. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Underdog Protocol. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Generate Claim Transaction](actions/generate-claim-transaction.md) | POST | Creates a claim transaction in Underdog Protocol for an NFT. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Underdog Protocol. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves a list of transactions from Underdog Protocol. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Underdog Protocol. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Underdog Protocol. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Underdog Protocol. |

