# Referral Rock: Native API Reference

A consolidated summary of Referral Rock's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://api.referralrock.com/help
- **API base URL:** `https://api.referralrock.com`

## Authentication

### Basic Authentication

Use your Referral Rock public and private API keys with Basic auth.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://api.referralrock.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size (default 30). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Hook](actions/create-hook.md) | `POST /api/hooks` | [docs](https://api.referralrock.com/Help/Api/POST-api-hooks) |
| [Create Member](actions/create-member.md) | `POST /api/members` | [docs](https://api.referralrock.com/Help/Api/POST-api-members_shouldSendEmail) |
| [Create Member Access URLs](actions/create-member-access-urls.md) | `POST /api/memberaccessurls` | [docs](https://api.referralrock.com/Help/Api/POST-api-memberaccessurls) |
| [Create Payout Transactions](actions/create-payout-transactions.md) | `POST /api/payouts/transactions` | [docs](https://api.referralrock.com/Help/Api/POST-api-payouts-transactions_overrideIneligible) |
| [Create Referral](actions/create-referral.md) | `POST /api/referrals` | [docs](https://api.referralrock.com/Help/Api/POST-api-referrals) |
| [Create Rewards](actions/create-rewards.md) | `POST /api/rewards` | [docs](https://api.referralrock.com/Help/Api/POST-api-rewards) |
| [Delete Hook](actions/delete-hook.md) | `DELETE /api/hooks` | [docs](https://api.referralrock.com/Help/Api/DELETE-api-hooks) |
| [Delete Members](actions/delete-members.md) | `POST /api/members/remove` | [docs](https://api.referralrock.com/Help/Api/POST-api-members-remove) |
| [Delete Referrals](actions/delete-referrals.md) | `POST /api/referral/remove` | [docs](https://api.referralrock.com/Help/Api/POST-api-referral-remove) |
| [Delete Rewards](actions/delete-rewards.md) | `POST /api/rewards/remove` | [docs](https://api.referralrock.com/Help/Api/POST-api-rewards-remove) |
| [Get Member Statistics](actions/get-member-statistics.md) | `GET /api/memberstats/getsingle` | [docs](https://api.referralrock.com/Help/Api/GET-api-memberstats-getsingle_query_timePeriod) |
| [Get Program](actions/get-program.md) | `GET /api/program/getsingle` | [docs](https://api.referralrock.com/Help/Api/GET-api-program-getsingle_programName) |
| [Get Referral](actions/get-referral.md) | `GET /api/referral/single` | [docs](https://api.referralrock.com/Help/Api/GET-api-referral-single_email_referralId_externalId) |
| [Issue Reward](actions/issue-reward.md) | `POST /api/rewards/issue` | [docs](https://api.referralrock.com/Help/Api/POST-api-rewards-issue_overrideIneligible) |
| [List Members](actions/list-members.md) | `GET /api/members` | [docs](https://api.referralrock.com/Help/Api/GET-api-members_programId_query_showDisabled_sort_dateFrom_dateTo_offset_count) |
| [List Payout Transactions](actions/list-payout-transactions.md) | `GET /api/payouts/transactions` | [docs](https://api.referralrock.com/Help/Api/GET-api-payouts-transactions_recipientId_transactionId) |
| [List Payouts](actions/list-payouts.md) | `GET /api/payouts` | [docs](https://api.referralrock.com/Help/Api/GET-api-payouts-id) |
| [List Pending Payouts](actions/list-pending-payouts.md) | `GET /api/payouts/pending` | [docs](https://api.referralrock.com/Help/Api/GET-api-payouts-pending_memberId_recipientId_includeIneligible) |
| [List Programs](actions/list-programs.md) | `GET /api/programs` | [docs](https://api.referralrock.com/Help/Api/GET-api-programs_programId_offset_count) |
| [List Referrals](actions/list-referrals.md) | `GET /api/referrals` | [docs](https://api.referralrock.com/Help/Api/GET-api-referrals_programId_query_memberId_sort_dateFrom_dateTo_status_offset_count) |
| [List Reward Rules](actions/list-reward-rules.md) | `GET /api/rewardrules` | [docs](https://api.referralrock.com/Help/Api/GET-api-rewardrules_programId) |
| [List Rewards](actions/list-rewards.md) | `GET /api/rewards` | [docs](https://api.referralrock.com/Help/Api/GET-api-rewards_programId_memberId_query_status_sort_dateFrom_dateTo_offset_count) |
| [Update Members](actions/update-members.md) | `POST /api/members/update` | [docs](https://api.referralrock.com/Help/Api/POST-api-members-update) |
| [Update Referrals](actions/update-referrals.md) | `POST /api/referral/update` | [docs](https://api.referralrock.com/Help/Api/POST-api-referral-update) |
| [Update Rewards](actions/update-rewards.md) | `POST /api/rewards/update` | [docs](https://api.referralrock.com/Help/Api/POST-api-rewards-update) |
