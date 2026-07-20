# Solana: Native API Reference

A consolidated summary of Solana's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://solana.com/docs/rpc
- **API base URL:** `https://api.mainnet-beta.solana.com`

## Authentication

### No Auth

Public Solana RPC endpoints require no credentials

This API does not require request authentication.

[Official authentication documentation](https://solana.com/docs/rpc)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Block Height](actions/get-block-height.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getblockheight) |
| [Get Block Production](actions/get-block-production.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getblockproduction) |
| [Get Cluster Nodes](actions/get-cluster-nodes.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getclusternodes) |
| [Get Epoch Info](actions/get-epoch-info.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getepochinfo) |
| [Get Epoch Schedule](actions/get-epoch-schedule.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getepochschedule) |
| [Get First Available Block](actions/get-first-available-block.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getfirstavailableblock) |
| [Get Genesis Hash](actions/get-genesis-hash.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getgenesishash) |
| [Get Health](actions/get-health.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/gethealth) |
| [Get Highest Snapshot Slot](actions/get-highest-snapshot-slot.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/gethighestsnapshotslot) |
| [Get Identity](actions/get-identity.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getidentity) |
| [Get Inflation Governor](actions/get-inflation-governor.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getinflationgovernor) |
| [Get Inflation Rate](actions/get-inflation-rate.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getinflationrate) |
| [Get Largest Accounts](actions/get-largest-accounts.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getlargestaccounts) |
| [Get Latest Blockhash](actions/get-latest-blockhash.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getlatestblockhash) |
| [Get Leader Schedule](actions/get-leader-schedule.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getleaderschedule) |
| [Get Max Retransmit Slot](actions/get-max-retransmit-slot.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getmaxretransmitslot) |
| [Get Max Shred Insert Slot](actions/get-max-shred-insert-slot.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getmaxshredinsertslot) |
| [Get Recent Performance Samples](actions/get-recent-performance-samples.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getrecentperformancesamples) |
| [Get Recent Prioritization Fees](actions/get-recent-prioritization-fees.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getrecentprioritizationfees) |
| [Get Slot](actions/get-slot.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getslot) |
| [Get Slot Leader](actions/get-slot-leader.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getslotleader) |
| [Get Stake Minimum Delegation](actions/get-stake-minimum-delegation.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getstakeminimumdelegation) |
| [Get Supply](actions/get-supply.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getsupply) |
| [Get Transaction Count](actions/get-transaction-count.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/gettransactioncount) |
| [Get Version](actions/get-version.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getversion) |
| [Get Vote Accounts](actions/get-vote-accounts.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/getvoteaccounts) |
| [Minimum Ledger Slot](actions/minimum-ledger-slot.md) | `POST /` | [docs](https://solana.com/docs/rpc/http/minimumledgerslot) |
