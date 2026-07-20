# Vouchery.io: Native API Reference

A consolidated summary of Vouchery.io's API configuration and 42 documented operations, with links to official documentation.

- **Official docs:** https://docs.vouchery.io/reference/getting-started-with-vouchery-api
- **API base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`

## Authentication

### API Key

Authenticate with a Vouchery API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.vouchery.io/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (42 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Redemption By Redemption ID](actions/cancel-redemption-by-redemption-id.md) | `DELETE /redemptions/:redemption_id` | [docs](https://docs.vouchery.io/reference/deleteapiv21redemptionsredemptionid) |
| [Confirm Redemption By Transaction ID](actions/confirm-redemption-by-transaction-id.md) | `PUT /redemptions/confirm` | [docs](https://docs.vouchery.io/reference/putapiv21redemptionsconfirm) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://docs.vouchery.io/reference/postapiv21campaigns) |
| [Create Campaign Reward](actions/create-campaign-reward.md) | `POST /campaigns/:campaign_id/rewards` | [docs](https://docs.vouchery.io/reference/postapiv21campaignscampaignidrewards) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://docs.vouchery.io/reference/postapiv21customers) |
| [Create Redemption](actions/create-redemption.md) | `POST /vouchers/:code/redemptions` | [docs](https://docs.vouchery.io/reference/postapiv21voucherscoderedemptions) |
| [Create Rule](actions/create-rule.md) | `POST /campaigns/:campaign_id/rules` | [docs](https://docs.vouchery.io/reference/postapiv21campaignscampaignidrules) |
| [Create Voucher](actions/create-voucher.md) | `POST /campaigns/:campaign_id/vouchers` | [docs](https://docs.vouchery.io/reference/postapiv21campaignscampaignidvouchers) |
| [Create Workflow](actions/create-workflow.md) | `POST /workflows` | [docs](https://docs.vouchery.io/reference/postapiv21workflows) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaigns/:campaign_id` | [docs](https://docs.vouchery.io/reference/deleteapiv21campaignscampaignid) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /workflows/:workflow_id` | [docs](https://docs.vouchery.io/reference/deleteapiv21workflowsworkflowid) |
| [Distribute Campaign Vouchers](actions/distribute-campaign-vouchers.md) | `GET /campaigns/:campaign_id/vouchers/distribute` | [docs](https://docs.vouchery.io/reference/getapiv21campaignscampaignidvouchersdistribute) |
| [Find Customers By Segment](actions/find-customers-by-segment.md) | `POST /customers/find` | [docs](https://docs.vouchery.io/reference/postapiv21customersfind) |
| [Generate Voucher Code](actions/generate-voucher-code.md) | `POST /campaigns/:campaign_id/generate-voucher-code` | [docs](https://docs.vouchery.io/reference/postapiv21campaignscampaignidgeneratevouchercode) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaign_id` | [docs](https://docs.vouchery.io/reference/getapiv21campaignscampaignid) |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | `GET /campaigns/:campaign_id/stats` | [docs](https://docs.vouchery.io/reference/getapiv21campaignscampaignidstats) |
| [Get Current User and Project](actions/get-current-user-and-project.md) | `GET /me` | [docs](https://docs.vouchery.io/reference/getapiv21me) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:identifier` | [docs](https://docs.vouchery.io/reference/getapiv21customersidentifier) |
| [Get Redemption](actions/get-redemption.md) | `GET /redemptions/:redemption_id` | [docs](https://docs.vouchery.io/reference/getapiv21redemptionsredemptionid) |
| [Get Reward](actions/get-reward.md) | `GET /rewards/:id` | [docs](https://docs.vouchery.io/reference/getapiv21rewardsid) |
| [Get Rule](actions/get-rule.md) | `GET /rules/:id` | [docs](https://docs.vouchery.io/reference/getapiv21rulesid) |
| [Get Voucher](actions/get-voucher.md) | `GET /vouchers/:code` | [docs](https://docs.vouchery.io/reference/getapiv21voucherscode) |
| [Get Voucher Details](actions/get-voucher-details.md) | `GET /vouchers/:code/extended` | [docs](https://docs.vouchery.io/reference/getapiv21voucherscodeextended) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/:workflow_id` | [docs](https://docs.vouchery.io/reference/getapiv21workflowsworkflowid) |
| [List Aggregated Campaign Statistics](actions/list-aggregated-campaign-statistics.md) | `GET /campaigns/aggregated_statistics` | [docs](https://docs.vouchery.io/reference/getapiv21campaignsaggregatedstatistics) |
| [List Available Events](actions/list-available-events.md) | `GET /event-types` | [docs](https://docs.vouchery.io/reference/getapiv21eventtypes) |
| [List Available Vouchers For Customer](actions/list-available-vouchers-for-customer.md) | `GET /customers/:identifier/available-vouchers` | [docs](https://docs.vouchery.io/reference/getapiv21customersidentifieravailablevouchers) |
| [List Campaign Redemptions](actions/list-campaign-redemptions.md) | `GET /campaigns/:campaign_id/redemptions` | [docs](https://docs.vouchery.io/reference/getapiv21campaignscampaignidredemptions) |
| [List Campaign Rewards](actions/list-campaign-rewards.md) | `GET /campaigns/:campaign_id/rewards` | [docs](https://docs.vouchery.io/reference/getapiv21campaignscampaignidrewards) |
| [List Campaign Rules](actions/list-campaign-rules.md) | `GET /campaigns/:campaign_id/rules` | [docs](https://docs.vouchery.io/reference/getapiv21campaignscampaignidrules) |
| [List Campaign Statistics](actions/list-campaign-statistics.md) | `GET /campaigns/stats` | [docs](https://docs.vouchery.io/reference/getapiv21campaignsstats) |
| [List Campaign Vouchers](actions/list-campaign-vouchers.md) | `GET /campaigns/:campaign_id/vouchers` | [docs](https://docs.vouchery.io/reference/getapiv21campaignscampaignidvouchers) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://docs.vouchery.io/reference/getapiv21campaigns) |
| [List Customer Redemptions](actions/list-customer-redemptions.md) | `GET /customers/:identifier/redemptions` | [docs](https://docs.vouchery.io/reference/getapiv21customersidentifierredemptions) |
| [List Customer Vouchers](actions/list-customer-vouchers.md) | `GET /customers/:identifier/vouchers` | [docs](https://docs.vouchery.io/reference/getapiv21customersidentifiervouchers) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.vouchery.io/reference/getapiv21customers) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://docs.vouchery.io/reference/getapiv21workflows) |
| [Update Campaign](actions/update-campaign.md) | `PUT /campaigns/:campaign_id` | [docs](https://docs.vouchery.io/reference/putapiv21campaignscampaignid) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:identifier` | [docs](https://docs.vouchery.io/reference/putapiv21customersidentifier) |
| [Update Reward](actions/update-reward.md) | `PUT /rewards/:id` | [docs](https://docs.vouchery.io/reference/putapiv21rewardsid) |
| [Update Rule](actions/update-rule.md) | `PUT /rules/:id` | [docs](https://docs.vouchery.io/reference/putapiv21rulesid) |
| [Validate Voucher](actions/validate-voucher.md) | `PUT /vouchers/:code/validate` | [docs](https://docs.vouchery.io/reference/putapiv21voucherscodevalidate) |
