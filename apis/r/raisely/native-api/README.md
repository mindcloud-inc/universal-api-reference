# Raisely: Native API Reference

A consolidated summary of Raisely's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.raisely.com/reference
- **OpenAPI specification:** https://api.raisely.com/v3/api-docs
- **API base URL:** `https://api.raisely.com/v3`

## Authentication

### API Key

Authenticate Raisely with a server-side API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.raisely.com/docs/authentication-1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The total page count is read from `pagination.pages`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Donation](actions/create-donation.md) | `POST /donations` | [docs](https://developers.raisely.com/reference/postdonations) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscriptions` | [docs](https://developers.raisely.com/reference/postsubscriptions) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaign` | [docs](https://developers.raisely.com/reference/getcampaign) |
| [Get Donation](actions/get-donation.md) | `GET /donations/:uuid` | [docs](https://developers.raisely.com/reference/getdonation) |
| [Get Profile](actions/get-profile.md) | `GET /profiles/:path` | [docs](https://developers.raisely.com/reference/getprofile) |
| [Get Subscription](actions/get-subscription.md) | `GET /subscriptions/:uuid` | [docs](https://developers.raisely.com/reference/getsubscription) |
| [Get User](actions/get-user.md) | `GET /users/:uuid` | [docs](https://developers.raisely.com/reference/getuser) |
| [List Campaign Donations](actions/list-campaign-donations.md) | `GET /campaigns/:campaign/donations` | [docs](https://developers.raisely.com/reference/getcampaignsdonations) |
| [List Campaign Profiles](actions/list-campaign-profiles.md) | `GET /campaigns/:campaign/profiles` | [docs](https://developers.raisely.com/reference/getcampaignsprofiles) |
| [List Campaign Subscriptions](actions/list-campaign-subscriptions.md) | `GET /campaigns/:campaign/subscriptions` | [docs](https://developers.raisely.com/reference/getcampaignssubscriptions) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://developers.raisely.com/reference/getcampaigns) |
| [List Donations](actions/list-donations.md) | `GET /donations` | [docs](https://developers.raisely.com/reference/getdonations) |
| [List Profile Members](actions/list-profile-members.md) | `GET /profiles/:path/members` | [docs](https://developers.raisely.com/reference/getprofilesmembers) |
| [List Profiles](actions/list-profiles.md) | `GET /profiles` | [docs](https://developers.raisely.com/reference/getprofiles) |
| [List Subscription Donations](actions/list-subscription-donations.md) | `GET /subscriptions/:uuid/donations` | [docs](https://developers.raisely.com/reference/getsubscriptionsdonations) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://developers.raisely.com/reference/getsubscriptions) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.raisely.com/reference/getusers) |
| [Resend Donation Receipt](actions/resend-donation-receipt.md) | `POST /donations/:uuid/resend` | [docs](https://developers.raisely.com/reference/postdonationsresend) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /campaigns/:campaign` | [docs](https://developers.raisely.com/reference/patchcampaign) |
| [Update Donation](actions/update-donation.md) | `PATCH /donations/:uuid` | [docs](https://developers.raisely.com/reference/patchdonation) |
| [Update Profile](actions/update-profile.md) | `PATCH /profiles/:path` | [docs](https://developers.raisely.com/reference/patchprofile) |
| [Update Subscription](actions/update-subscription.md) | `PATCH /subscriptions/:uuid` | [docs](https://developers.raisely.com/reference/patchsubscription) |
| [Update User](actions/update-user.md) | `PATCH /users/:uuid` | [docs](https://developers.raisely.com/reference/patchuser) |
| [Upsert User](actions/upsert-user.md) | `POST /users/upsert` | [docs](https://developers.raisely.com/reference/postusersupsert) |
