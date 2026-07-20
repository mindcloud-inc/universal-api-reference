# Yotpo Loyalty & Referrals: Native API Reference

A consolidated summary of Yotpo Loyalty & Referrals's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://loyaltyapi.yotpo.com/reference/welcome
- **API base URL:** `https://loyalty.yotpo.com`

## Authentication

### API Key

Authenticate with Yotpo Loyalty GUID and API key headers.

### Credentials

- **API Key:** `apiKey` · required
- **GUID:** `guid` · required · Your Yotpo Loyalty & Referrals GUID.

Send these headers with each API request:

```http
x-guid: <guid>
x-api-key: <apiKey>
```

[Official authentication documentation](https://loyaltyapi.yotpo.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `metadata.next_page_info`.

## Pagination

Use `per_page` in the query string to set the page size. Use `page_info` in the query string as the pagination cursor.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Adjust Customer Points Balance](actions/adjust-customer-points-balance.md) | `POST /api/v2/points/adjust` | [docs](https://loyaltyapi.yotpo.com/reference/adjust-a-customers-point-balance) |
| [Anonymize User](actions/anonymize-user.md) | `DELETE /api/v2/privacy/data` | [docs](https://loyaltyapi.yotpo.com/reference/anonymize-user) |
| [Approve Redemption Cancellation](actions/approve-redemption-cancellation.md) | `POST /api/v2/redemptions/:point_redemption_id/cancellation_completed` | [docs](https://loyaltyapi.yotpo.com/reference/approve-redemption-cancellation) |
| [Check Data Exists](actions/check-data-exists.md) | `GET /api/v2/privacy/data/exists` | [docs](https://loyaltyapi.yotpo.com/reference/data-exists) |
| [Create or Update Customer Records](actions/create-or-update-customer-records.md) | `POST /api/v2/customers` | [docs](https://loyaltyapi.yotpo.com/reference/createupdate-customer-records) |
| [Create Order](actions/create-order.md) | `POST /api/v2/orders` | [docs](https://loyaltyapi.yotpo.com/reference/create-order) |
| [Create Redemption](actions/create-redemption.md) | `POST /api/v2/redemptions` | [docs](https://loyaltyapi.yotpo.com/reference/create-redemption) |
| [Create Refund](actions/create-refund.md) | `POST /api/v2/refunds` | [docs](https://loyaltyapi.yotpo.com/reference/create-refund) |
| [Fetch Customer Details](actions/fetch-customer-details.md) | `GET /api/v2/customers` | [docs](https://loyaltyapi.yotpo.com/reference/fetch-customer-details) |
| [Fetch Recently Updated Customers](actions/fetch-recently-updated-customers.md) | `GET /api/v2/customers/recent` | [docs](https://loyaltyapi.yotpo.com/reference/fetch-all-recently-updated-customers) |
| [Fetch VIP Tiers](actions/fetch-vip-tiers.md) | `GET /api/v2/vip_tiers` | [docs](https://loyaltyapi.yotpo.com/reference/fetch-vip-tiers) |
| [Get Active Campaigns](actions/get-active-campaigns.md) | `GET /api/v2/campaigns` | [docs](https://loyaltyapi.yotpo.com/reference/get-active-campaigns) |
| [Get Active Redemption Options](actions/get-active-redemption-options.md) | `GET /api/v2/redemption_options` | [docs](https://loyaltyapi.yotpo.com/reference/fetch-active-redemption-options) |
| [Get Customer Anniversary](actions/get-customer-anniversary.md) | `GET /api/v2/customer_anniversary` | [docs](https://loyaltyapi.yotpo.com/reference/get-customer-anniversary) |
| [Get Redemption Code Data](actions/get-redemption-code-data.md) | `GET /api/v2/redemption_codes` | [docs](https://loyaltyapi.yotpo.com/reference/get-redemption-code-data) |
| [Get User Data](actions/get-user-data.md) | `GET /api/v2/privacy/data` | [docs](https://loyaltyapi.yotpo.com/reference/user-data) |
| [Identify Referrer](actions/identify-referrer.md) | `POST /api/v2/referral/referrer` | [docs](https://loyaltyapi.yotpo.com/reference/identify-referrer) |
| [Remove Customer Anniversary](actions/remove-customer-anniversary.md) | `DELETE /api/v2/customer_anniversary` | [docs](https://loyaltyapi.yotpo.com/reference/remove-customer-anniversary) |
| [Send Referral Emails](actions/send-referral-emails.md) | `POST /api/v2/referral/share` | [docs](https://loyaltyapi.yotpo.com/reference/send-referral-emails-1) |
| [Set Customer Birthday](actions/set-customer-birthday.md) | `POST /api/v2/customer_birthdays` | [docs](https://loyaltyapi.yotpo.com/reference/set-customer-birthday) |
| [Set or Update Customer Anniversary](actions/set-or-update-customer-anniversary.md) | `POST /api/v2/customer_anniversary` | [docs](https://loyaltyapi.yotpo.com/reference/createupdate-customer-anniversary) |
| [Upload Coupon Codes](actions/upload-coupon-codes.md) | `POST /api/v2/redemption_codes` | [docs](https://loyaltyapi.yotpo.com/reference/add-coupon-codes) |
