# <img src="https://images.mindcloud.co/apps/icons/explodely_1774031343606.png" alt="Explodely logo" width="28" height="28"> Explodely: Universal API

Manage Explodely affiliates, payouts, contracts, and rebills

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/explodely/latest
- **Category:** Commerce
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://explodely.com/
- **Vendor API docs:** https://docs.explodely.com/api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Add Affiliate To Affiliate Referral Contract](actions/add-affiliate-to-affiliate-referral-contract.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/explodely/latest/actions/add-affiliate-to-affiliate-referral-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractId": "12345",
  "affiliateUsername": "affiliate_username"
}'
```

## Actions (8)

### Affiliate Referral Contract

| Action | Method | Description |
| --- | --- | --- |
| [Add Affiliate To Affiliate Referral Contract](actions/add-affiliate-to-affiliate-referral-contract.md) | PUT | Updates an affiliate referral contract in Explodely by adding an affiliate. |
| [Create Affiliate Referral Contract](actions/create-affiliate-referral-contract.md) | POST | Creates a new affiliate referral contract in Explodely. |
| [Update Affiliate Referral Contract](actions/update-affiliate-referral-contract.md) | PUT | Updates an affiliate referral contract in Explodely. |

### Affiliate User

| Action | Method | Description |
| --- | --- | --- |
| [Create Affiliate User](actions/create-affiliate-user.md) | POST | Creates a new affiliate user in Explodely. |

### Private Affiliate Payout

| Action | Method | Description |
| --- | --- | --- |
| [List Private Affiliate Payouts](actions/list-private-affiliate-payouts.md) | POST |  |
| [Update Private Affiliate Payout](actions/update-private-affiliate-payout.md) | PUT | Updates a private affiliate payout in Explodely. |

### Rebill

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Rebill](actions/cancel-rebill.md) | DELETE | Cancels rebills in Explodely by main order ID. |
| [Pause Rebill](actions/pause-rebill.md) | PUT | Updates a rebill in Explodely by delaying the next charge. |

