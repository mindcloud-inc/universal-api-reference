# KYVE: Native API Reference

A consolidated summary of KYVE's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.kyve.network/build/web3-devs/endpoints
- **OpenAPI specification:** https://api.kyve.network/static/openapi.yml
- **API base URL:** `https://api.kyve.network`

## Authentication

### No authentication

KYVE public REST endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://docs.kyve.network/build/web3-devs/endpoints)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pagination.limit` in the query string to set the page size. Use `pagination.offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Can Propose](actions/check-can-propose.md) | `GET /kyve/query/v1beta1/can_propose/{pool_id}/{staker}/{proposer}/{from_index}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Check Can Validate](actions/check-can-validate.md) | `GET /kyve/query/v1beta1/can_validate/{pool_id}/{pool_address}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Check Can Vote](actions/check-can-vote.md) | `GET /kyve/query/v1beta1/can_vote/{pool_id}/{staker}/{voter}/{storage_id}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Count Stakers By Pool](actions/count-stakers-by-pool.md) | `GET /kyve/query/v1/stakers_by_pool_count` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Account Assets](actions/get-account-assets.md) | `GET /kyve/query/v1beta1/account_assets/{address}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Bundle Parameters](actions/get-bundle-parameters.md) | `GET /kyve/bundles/v1beta1/params` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Current Vote Status](actions/get-current-vote-status.md) | `GET /kyve/query/v1beta1/current_vote_status/{pool_id}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Finalized Bundle](actions/get-finalized-bundle.md) | `GET /kyve/v1/bundles/{pool_id}/{id}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Funder](actions/get-funder.md) | `GET /kyve/query/v1beta1/funder/{address}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Global Parameters](actions/get-global-parameters.md) | `GET /kyve/global/v1beta1/params` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Last Tokenize Share Record ID](actions/get-last-tokenize-share-record-id.md) | `GET /kyve/liquid/v1beta1/last_tokenize_share_record_id` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Latest Block](actions/get-latest-block.md) | `GET /cosmos/base/tendermint/v1beta1/blocks/latest` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Liquid Parameters](actions/get-liquid-parameters.md) | `GET /kyve/liquid/v1beta1/params` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Liquid Validator](actions/get-liquid-validator.md) | `GET /kyve/liquid/v1beta1/liquid_validator/{validator_addr}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Pool](actions/get-pool.md) | `GET /kyve/query/v1beta1/pool/{id}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Pools Parameters](actions/get-pools-parameters.md) | `GET /kyve/query/v1beta1/params` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Staker](actions/get-staker.md) | `GET /kyve/query/v1/staker/{address}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Stakers Parameters](actions/get-stakers-parameters.md) | `GET /kyve/stakers/v1/params` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Team Info](actions/get-team-info.md) | `GET /kyve/team/v1beta1/team_info` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Team Vesting Account](actions/get-team-vesting-account.md) | `GET /kyve/team/v1beta1/team_vesting_account/{id}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Team Vesting Status](actions/get-team-vesting-status.md) | `GET /kyve/team/v1beta1/team_vesting_status/{id}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Team Vesting Status By Time](actions/get-team-vesting-status-by-time.md) | `GET /kyve/team/v1beta1/team_vesting_status_by_time/{id}/{time}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Tokenize Share Lock Info](actions/get-tokenize-share-lock-info.md) | `GET /kyve/liquid/v1beta1/tokenize_share_lock_info/{address}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Tokenize Share Record By Denom](actions/get-tokenize-share-record-by-denom.md) | `GET /kyve/liquid/v1beta1/tokenize_share_record_by_denom/{denom}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Tokenize Share Record By ID](actions/get-tokenize-share-record-by-id.md) | `GET /kyve/liquid/v1beta1/tokenize_share_record_by_id/{id}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Tokenize Share Record Rewards](actions/get-tokenize-share-record-rewards.md) | `GET /kyve/liquid/v1beta1/{owner_address}/tokenize_share_record_rewards` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Total Liquid Staked](actions/get-total-liquid-staked.md) | `GET /kyve/liquid/v1beta1/total_liquid_staked` | [docs](https://api.kyve.network/static/openapi.yml) |
| [Get Total Tokenized Staked Assets](actions/get-total-tokenized-staked-assets.md) | `GET /kyve/liquid/v1beta1/total_tokenize_shared_assets` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Account Funded Pools](actions/list-account-funded-pools.md) | `GET /kyve/query/v1beta1/account_funded_list/{address}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Finalized Bundles](actions/list-finalized-bundles.md) | `GET /kyve/v1/bundles/{pool_id}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Funders](actions/list-funders.md) | `GET /kyve/query/v1beta1/funders` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Fundings By Funder](actions/list-fundings-by-funder.md) | `GET /kyve/query/v1beta1/fundings_by_funder/{address}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Fundings By Pool](actions/list-fundings-by-pool.md) | `GET /kyve/query/v1beta1/fundings_by_pool/{pool_id}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Liquid Validators](actions/list-liquid-validators.md) | `GET /kyve/liquid/v1beta1/liquid_validators` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Pools](actions/list-pools.md) | `GET /kyve/query/v1beta1/pools` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Stakers](actions/list-stakers.md) | `GET /kyve/query/v1/stakers` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Stakers By Pool](actions/list-stakers-by-pool.md) | `GET /kyve/query/v1/stakers_by_pool/{pool_id}` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Team Vesting Accounts](actions/list-team-vesting-accounts.md) | `GET /kyve/team/v1beta1/team_vesting_accounts` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Tokenize Share Records](actions/list-tokenize-share-records.md) | `GET /kyve/liquid/v1beta1/tokenize_share_records` | [docs](https://api.kyve.network/static/openapi.yml) |
| [List Tokenize Share Records Owned](actions/list-tokenize-share-records-owned.md) | `GET /kyve/liquid/v1beta1/tokenize_share_record_owned/{owner}` | [docs](https://api.kyve.network/static/openapi.yml) |
