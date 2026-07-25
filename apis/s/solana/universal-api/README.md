# <img src="https://images.mindcloud.co/apps/icons/solana-logo_1776116156998.png" alt="Solana logo" width="28" height="28"> Solana: Universal API

Solana JSON-RPC API

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/solana/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://solana.com/
- **Vendor API docs:** https://solana.com/docs/rpc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Block Height](actions/get-block-height.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solana/latest/actions/get-block-height?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Get Block Height](actions/get-block-height.md) | GET | Retrieves the current block height from Solana. |
| [Get Block Production](actions/get-block-production.md) | GET | Retrieves block production details from Solana. |
| [Get Block Production (Draft Variant)](actions/get-block-production-draft-variant.md) | GET | Retrieves block production details from Solana. |
| [Get Cluster Nodes](actions/get-cluster-nodes.md) | GET | Retrieves cluster node details from Solana. |
| [Get Epoch Info](actions/get-epoch-info.md) | GET | Retrieves current epoch information from Solana. |
| [Get Epoch Schedule](actions/get-epoch-schedule.md) | GET | Retrieves the epoch schedule from Solana. |
| [Get First Available Block](actions/get-first-available-block.md) | GET | Retrieves the first available block from Solana. |
| [Get Genesis Hash](actions/get-genesis-hash.md) | GET | Retrieves the genesis hash from Solana. |
| [Get Health](actions/get-health.md) | GET | Retrieves the node health status from Solana. |
| [Get Highest Snapshot Slot](actions/get-highest-snapshot-slot.md) | GET | Retrieves highest snapshot slots from Solana. |
| [Get Identity](actions/get-identity.md) | GET | Retrieves the node identity from Solana. |
| [Get Inflation Governor](actions/get-inflation-governor.md) | GET | Retrieves inflation governor settings from Solana. |
| [Get Inflation Rate](actions/get-inflation-rate.md) | GET | Retrieves the current inflation rate from Solana. |
| [Get Largest Accounts](actions/get-largest-accounts.md) | GET | Retrieves the largest accounts from Solana. |
| [Get Latest Blockhash](actions/get-latest-blockhash.md) | GET | Retrieves the latest blockhash from Solana. |
| [Get Leader Schedule](actions/get-leader-schedule.md) | GET | Retrieves the leader schedule from Solana. |
| [Get Max Retransmit Slot](actions/get-max-retransmit-slot.md) | GET | Retrieves the max retransmit slot from Solana. |
| [Get Max Shred Insert Slot](actions/get-max-shred-insert-slot.md) | GET | Retrieves the max shred insert slot from Solana. |
| [Get Recent Performance Samples](actions/get-recent-performance-samples.md) | GET | Retrieves recent performance samples from Solana. |
| [Get Recent Performance Samples (Draft Variant)](actions/get-recent-performance-samples-draft-variant.md) | GET | Retrieves recent performance samples from Solana. |
| [Get Recent Prioritization Fees](actions/get-recent-prioritization-fees.md) | GET | Retrieves recent prioritization fees from Solana. |
| [Get Recent Prioritization Fees (Draft Variant)](actions/get-recent-prioritization-fees-draft-variant.md) | GET | Retrieves recent prioritization fees from Solana. |
| [Get Slot](actions/get-slot.md) | GET | Retrieves the current slot from Solana. |
| [Get Slot Leader](actions/get-slot-leader.md) | GET | Retrieves the current slot leader from Solana. |
| [Get Stake Minimum Delegation](actions/get-stake-minimum-delegation.md) | GET | Retrieves the minimum stake delegation from Solana. |
| [Get Supply](actions/get-supply.md) | GET | Retrieves the current token supply from Solana. |
| [Get Transaction Count](actions/get-transaction-count.md) | GET | Retrieves the transaction count from Solana. |
| [Get Version](actions/get-version.md) | GET | Retrieves node version details from Solana. |
| [Get Vote Accounts](actions/get-vote-accounts.md) | GET | Retrieves vote accounts from Solana. |
| [Minimum Ledger Slot](actions/minimum-ledger-slot.md) | GET | Retrieves the minimum ledger slot from Solana. |

