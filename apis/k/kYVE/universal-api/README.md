# <img src="https://images.mindcloud.co/apps/icons/k-yve_1776793815346.png" alt="KYVE logo" width="28" height="28"> KYVE: Universal API

KYVE provides public access to validated blockchain data, including KYVE chain state and protocol data through official LCD REST endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kYVE/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kyve.network
- **Vendor API docs:** https://docs.kyve.network/build/web3-devs/endpoints

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Pools Parameters](actions/get-pools-parameters.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-pools-parameters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Assets](actions/get-account-assets.md) | GET |  |
| [List Account Funded Pools](actions/list-account-funded-pools.md) | GET |  |

### Bundles

| Action | Method | Description |
| --- | --- | --- |
| [Get Bundle Parameters](actions/get-bundle-parameters.md) | GET |  |
| [Get Finalized Bundle](actions/get-finalized-bundle.md) | GET |  |
| [List Finalized Bundles](actions/list-finalized-bundles.md) | GET |  |

### Chain

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Block](actions/get-latest-block.md) | GET |  |

### Funders

| Action | Method | Description |
| --- | --- | --- |
| [Get Funder](actions/get-funder.md) | GET |  |
| [List Funders](actions/list-funders.md) | GET |  |
| [List Fundings By Funder](actions/list-fundings-by-funder.md) | GET |  |
| [List Fundings By Pool](actions/list-fundings-by-pool.md) | GET |  |

### Global

| Action | Method | Description |
| --- | --- | --- |
| [Get Global Parameters](actions/get-global-parameters.md) | GET |  |

### Liquid Staking

| Action | Method | Description |
| --- | --- | --- |
| [Get Last Tokenize Share Record ID](actions/get-last-tokenize-share-record-id.md) | GET |  |
| [Get Liquid Parameters](actions/get-liquid-parameters.md) | GET |  |
| [Get Liquid Validator](actions/get-liquid-validator.md) | GET |  |
| [Get Tokenize Share Lock Info](actions/get-tokenize-share-lock-info.md) | GET |  |
| [Get Tokenize Share Record By Denom](actions/get-tokenize-share-record-by-denom.md) | GET |  |
| [Get Tokenize Share Record By ID](actions/get-tokenize-share-record-by-id.md) | GET |  |
| [Get Tokenize Share Record Rewards](actions/get-tokenize-share-record-rewards.md) | GET |  |
| [Get Total Liquid Staked](actions/get-total-liquid-staked.md) | GET |  |
| [Get Total Tokenized Staked Assets](actions/get-total-tokenized-staked-assets.md) | GET |  |
| [List Liquid Validators](actions/list-liquid-validators.md) | GET |  |
| [List Tokenize Share Records](actions/list-tokenize-share-records.md) | GET |  |
| [List Tokenize Share Records Owned](actions/list-tokenize-share-records-owned.md) | GET |  |

### Pools

| Action | Method | Description |
| --- | --- | --- |
| [Get Pool](actions/get-pool.md) | GET |  |
| [Get Pools Parameters](actions/get-pools-parameters.md) | GET |  |
| [List Pools](actions/list-pools.md) | GET |  |

### Stakers

| Action | Method | Description |
| --- | --- | --- |
| [Count Stakers By Pool](actions/count-stakers-by-pool.md) | GET |  |
| [Get Staker](actions/get-staker.md) | GET |  |
| [Get Stakers Parameters](actions/get-stakers-parameters.md) | GET |  |
| [List Stakers](actions/list-stakers.md) | GET |  |
| [List Stakers By Pool](actions/list-stakers-by-pool.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Info](actions/get-team-info.md) | GET |  |
| [Get Team Vesting Account](actions/get-team-vesting-account.md) | GET |  |
| [Get Team Vesting Status](actions/get-team-vesting-status.md) | GET |  |
| [Get Team Vesting Status By Time](actions/get-team-vesting-status-by-time.md) | GET |  |
| [List Team Vesting Accounts](actions/list-team-vesting-accounts.md) | GET |  |

### Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Can Validate](actions/check-can-validate.md) | GET |  |

### Voting

| Action | Method | Description |
| --- | --- | --- |
| [Check Can Propose](actions/check-can-propose.md) | GET |  |
| [Check Can Vote](actions/check-can-vote.md) | GET |  |
| [Get Current Vote Status](actions/get-current-vote-status.md) | GET |  |

