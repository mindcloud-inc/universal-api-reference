# <img src="https://images.mindcloud.co/apps/icons/yotpo-loyalty-referrals_1774279213928.png" alt="Yotpo Loyalty & Referrals logo" width="28" height="28"> Yotpo Loyalty & Referrals: Universal API

Manage loyalty customers, points, referrals, and redemptions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yotpoLoyaltyReferrals/latest
- **Category:** Commerce
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.yotpo.com
- **Vendor API docs:** https://loyaltyapi.yotpo.com/reference/welcome

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Recently Updated Customers](actions/fetch-recently-updated-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/fetch-recently-updated-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Campaigns](actions/get-active-campaigns.md) | GET | Retrieves active campaigns from Yotpo Loyalty & Referrals. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Customer Records](actions/create-or-update-customer-records.md) | PUT | Creates or updates customer records in Yotpo Loyalty & Referrals. |
| [Fetch Customer Details](actions/fetch-customer-details.md) | GET | Retrieves customer details from Yotpo Loyalty & Referrals. |
| [Fetch Recently Updated Customers](actions/fetch-recently-updated-customers.md) | GET | Retrieves recently updated customers from Yotpo Loyalty & Referrals. |

### Customer Anniversary

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Anniversary](actions/get-customer-anniversary.md) | GET | Retrieves a customer's anniversary from Yotpo Loyalty & Referrals. |
| [Remove Customer Anniversary](actions/remove-customer-anniversary.md) | DELETE | Deletes a customer's anniversary from Yotpo Loyalty & Referrals. |
| [Set or Update Customer Anniversary](actions/set-or-update-customer-anniversary.md) | PUT | Updates a customer's anniversary in Yotpo Loyalty & Referrals. |

### Customer Birthday

| Action | Method | Description |
| --- | --- | --- |
| [Set Customer Birthday](actions/set-customer-birthday.md) | PUT | Updates a customer's birthday in Yotpo Loyalty & Referrals. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates an order in Yotpo Loyalty & Referrals. |

### Points Balance

| Action | Method | Description |
| --- | --- | --- |
| [Adjust Customer Points Balance](actions/adjust-customer-points-balance.md) | PUT | Updates a customer's points balance in Yotpo Loyalty & Referrals. |

### Privacy Data

| Action | Method | Description |
| --- | --- | --- |
| [Anonymize User](actions/anonymize-user.md) | DELETE | Deletes and anonymizes user data in Yotpo Loyalty & Referrals. |
| [Check Data Exists](actions/check-data-exists.md) | GET | Checks whether user data exists in Yotpo Loyalty & Referrals. |
| [Get User Data](actions/get-user-data.md) | GET | Retrieves user data from Yotpo Loyalty & Referrals. |

### Redemption

| Action | Method | Description |
| --- | --- | --- |
| [Approve Redemption Cancellation](actions/approve-redemption-cancellation.md) | PUT | Approves a redemption cancellation in Yotpo Loyalty & Referrals. |
| [Create Redemption](actions/create-redemption.md) | POST | Creates a redemption in Yotpo Loyalty & Referrals. |

### Redemption Code

| Action | Method | Description |
| --- | --- | --- |
| [Get Redemption Code Data](actions/get-redemption-code-data.md) | GET | Retrieves redemption code data from Yotpo Loyalty & Referrals. |
| [Upload Coupon Codes](actions/upload-coupon-codes.md) | POST | Uploads coupon codes to Yotpo Loyalty & Referrals. |

### Redemption Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Redemption Options](actions/get-active-redemption-options.md) | GET | Retrieves active redemption options from Yotpo Loyalty & Referrals. |

### Referral

| Action | Method | Description |
| --- | --- | --- |
| [Identify Referrer](actions/identify-referrer.md) | POST | Finds or creates a referral link in Yotpo Loyalty & Referrals. |
| [Send Referral Emails](actions/send-referral-emails.md) | POST | Sends referral emails from Yotpo Loyalty & Referrals. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST | Creates a refund in Yotpo Loyalty & Referrals. |

### Vip Tier

| Action | Method | Description |
| --- | --- | --- |
| [Fetch VIP Tiers](actions/fetch-vip-tiers.md) | GET | Retrieves VIP tiers from Yotpo Loyalty & Referrals. |

