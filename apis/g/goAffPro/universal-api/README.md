# <img src="https://images.mindcloud.co/apps/icons/icon-square_1776102031900.png" alt="GoAffPro logo" width="28" height="28"> GoAffPro: Universal API

Manage affiliates, orders, payouts, and referral activity

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goAffPro/latest
- **Category:** Marketing
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://goaffpro.com/
- **Vendor API docs:** https://api.goaffpro.com/docs/admin/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Affiliates](actions/list-affiliates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-affiliates?connectionId=$CONNECTION_ID&limit=25&offset=0&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Affiliate Customer Connections

| Action | Method | Description |
| --- | --- | --- |
| [List Affiliate Customer Connections](actions/list-affiliate-customer-connections.md) | GET | Retrieves affiliate customer connections from GoAffPro. |

### Affiliates

| Action | Method | Description |
| --- | --- | --- |
| [Create Affiliate](actions/create-affiliate.md) | POST | Creates a new affiliate in GoAffPro. |
| [List Affiliates](actions/list-affiliates.md) | GET | Retrieves a list of affiliates from GoAffPro. |
| [Search Affiliates](actions/search-affiliates.md) | GET | Finds affiliates in GoAffPro by keyword. |
| [Update Affiliate](actions/update-affiliate.md) | PUT | Updates an existing affiliate in GoAffPro. |

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [List Affiliate Coupons](actions/list-affiliate-coupons.md) | GET | Retrieves an affiliate's coupons from GoAffPro. |
| [List Coupon Codes](actions/list-coupon-codes.md) | GET | Retrieves assigned coupon codes from GoAffPro. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves configured affiliate groups from GoAffPro. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a manual affiliate order and commission in GoAffPro. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of affiliate orders from GoAffPro. |
| [Recalculate Order Commission](actions/recalculate-order-commission.md) | PUT | Recalculates commission for an order in GoAffPro. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in GoAffPro. |

### Payment Requests

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Requests](actions/list-payment-requests.md) | GET | Retrieves affiliate payment requests from GoAffPro. |
| [Update Payment Request](actions/update-payment-request.md) | PUT | Updates an affiliate payment request in GoAffPro. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Request](actions/create-payment-request.md) | POST | Creates a new payment request in GoAffPro. |
| [List Payments](actions/list-payments.md) | GET | Retrieves payment history entries from GoAffPro. |

### Payouts

| Action | Method | Description |
| --- | --- | --- |
| [List Pending Payouts](actions/list-pending-payouts.md) | GET | Retrieves pending affiliate payouts from GoAffPro. |

### Referral Codes

| Action | Method | Description |
| --- | --- | --- |
| [List Affiliate Referral Codes](actions/list-affiliate-referral-codes.md) | GET | Retrieves an affiliate's referral codes from GoAffPro. |
| [Replace Affiliate Referral Codes](actions/replace-affiliate-referral-codes.md) | PUT | Replaces an affiliate's referral codes in GoAffPro. |

### Rewards

| Action | Method | Description |
| --- | --- | --- |
| [Give Reward](actions/give-reward.md) | POST | Creates a reward for an affiliate in GoAffPro. |
| [List Rewards](actions/list-rewards.md) | GET | Retrieves a list of affiliate rewards from GoAffPro. |
| [Update Reward](actions/update-reward.md) | PUT | Updates an existing reward in GoAffPro. |

### Traffic

| Action | Method | Description |
| --- | --- | --- |
| [List Traffic](actions/list-traffic.md) | GET | Retrieves affiliate traffic data from GoAffPro. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transaction log entries from GoAffPro. |

### Unpaid Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Unpaid Transactions](actions/list-unpaid-transactions.md) | GET | Retrieves unpaid affiliate transactions from GoAffPro. |

