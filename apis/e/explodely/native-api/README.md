# Explodely: Native API Reference

A consolidated summary of Explodely's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.explodely.com/api/introduction
- **API base URL:** `https://explodely.com/api/v1`

## Authentication

### Username + API Key

Authenticate with your Explodely username and API key.

### Credentials

- **API Key:** `apiKey` · required
- **Username:** `username` · required · Your Explodely seller account username.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.explodely.com/api/authentication)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Affiliate To Affiliate Referral Contract](actions/add-affiliate-to-affiliate-referral-contract.md) | `POST /aff` | [docs](https://docs.explodely.com/api/add-affiliate-to-affiliate-referral-contract) |
| [Cancel Rebill](actions/cancel-rebill.md) | `GET /rebill` | [docs](https://docs.explodely.com/api/cancel-rebill) |
| [Create Affiliate Referral Contract](actions/create-affiliate-referral-contract.md) | `POST /aff` | [docs](https://docs.explodely.com/api/create-affiliate-referral-contract) |
| [Create Affiliate User](actions/create-affiliate-user.md) | `POST /aff` | [docs](https://docs.explodely.com/api/create-affiliate-user) |
| [List Private Affiliate Payouts](actions/list-private-affiliate-payouts.md) | `GET /aff` | [docs](https://docs.explodely.com/api/private-affiliate-payouts) |
| [Pause Rebill](actions/pause-rebill.md) | `GET /rebill` | [docs](https://docs.explodely.com/api/pause-rebill-api) |
| [Update Affiliate Referral Contract](actions/update-affiliate-referral-contract.md) | `POST /aff` | [docs](https://docs.explodely.com/api/edit-affiliate-referral-contract) |
| [Update Private Affiliate Payout](actions/update-private-affiliate-payout.md) | `POST /aff` | [docs](https://docs.explodely.com/api/edit-private-affiliate-payout) |
