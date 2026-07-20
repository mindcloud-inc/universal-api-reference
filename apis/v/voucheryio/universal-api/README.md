# <img src="https://images.mindcloud.co/apps/icons/voucheryio_1775146873666.png" alt="Vouchery.io logo" width="28" height="28"> Vouchery.io: Universal API

Create and automate coupons, referrals, and loyalty promotions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/voucheryio/latest
- **Category:** Marketing
- **Actions:** 42
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.vouchery.io/
- **Vendor API docs:** https://docs.vouchery.io/reference/getting-started-with-vouchery-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User and Project](actions/get-current-user-and-project.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-current-user-and-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (42)

### Aggregated Campaign Statistics

| Action | Method | Description |
| --- | --- | --- |
| [List Aggregated Campaign Statistics](actions/list-aggregated-campaign-statistics.md) | GET |  |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [Delete Campaign](actions/delete-campaign.md) | DELETE |  |
| [Get Campaign](actions/get-campaign.md) | GET |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |
| [Update Campaign](actions/update-campaign.md) | PUT |  |

### Campaign Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | GET |  |
| [List Campaign Statistics](actions/list-campaign-statistics.md) | GET |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Distribute Campaign Vouchers](actions/distribute-campaign-vouchers.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Find Customers By Segment](actions/find-customers-by-segment.md) | GET |  |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Redemption By Redemption ID](actions/cancel-redemption-by-redemption-id.md) | DELETE |  |
| [Confirm Redemption By Transaction ID](actions/confirm-redemption-by-transaction-id.md) | PUT |  |
| [Create Redemption](actions/create-redemption.md) | POST |  |
| [Create Voucher](actions/create-voucher.md) | POST |  |
| [Generate Voucher Code](actions/generate-voucher-code.md) | POST |  |
| [Get Redemption](actions/get-redemption.md) | GET |  |
| [Get Voucher](actions/get-voucher.md) | GET |  |
| [Get Voucher Details](actions/get-voucher-details.md) | GET |  |
| [List Available Vouchers For Customer](actions/list-available-vouchers-for-customer.md) | GET |  |
| [List Campaign Redemptions](actions/list-campaign-redemptions.md) | GET |  |
| [List Campaign Vouchers](actions/list-campaign-vouchers.md) | GET |  |
| [List Customer Redemptions](actions/list-customer-redemptions.md) | GET |  |
| [List Customer Vouchers](actions/list-customer-vouchers.md) | GET |  |
| [Validate Voucher](actions/validate-voucher.md) | PUT |  |

### Reward

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign Reward](actions/create-campaign-reward.md) | POST |  |
| [Get Reward](actions/get-reward.md) | GET |  |
| [List Campaign Rewards](actions/list-campaign-rewards.md) | GET |  |
| [Update Reward](actions/update-reward.md) | PUT |  |

### Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create Rule](actions/create-rule.md) | POST |  |
| [Get Rule](actions/get-rule.md) | GET |  |
| [List Campaign Rules](actions/list-campaign-rules.md) | GET |  |
| [Update Rule](actions/update-rule.md) | PUT |  |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User and Project](actions/get-current-user-and-project.md) | GET |  |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST |  |
| [Delete Workflow](actions/delete-workflow.md) | DELETE |  |
| [Get Workflow](actions/get-workflow.md) | GET |  |
| [List Available Events](actions/list-available-events.md) | GET |  |
| [List Workflows](actions/list-workflows.md) | GET |  |

