# <img src="https://images.mindcloud.co/apps/icons/soundee_1773840122756.png" alt="Soundee logo" width="28" height="28"> Soundee: Universal API

Soundee is a social music platform that connects artists with producers and offers eCommerce and marketing tools for producers who sell beats.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/soundee/latest
- **Category:** Commerce
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://soundee.com
- **Vendor API docs:** https://soundee.readme.io/reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves your Soundee producer account details. |

### Cart Abandonment

| Action | Method | Description |
| --- | --- | --- |
| [Get Cart Abandonment](actions/get-cart-abandonment.md) | GET | Retrieves an abandoned cart from Soundee by ID or token. |
| [List Cart Abandonments](actions/list-cart-abandonments.md) | GET | Retrieves abandoned cart records from Soundee. |

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | POST | Creates a new coupon in Soundee. |
| [Get Coupon](actions/get-coupon.md) | GET | Retrieves a coupon code from Soundee. |
| [List Coupons](actions/list-coupons.md) | GET | Retrieves your coupon codes from Soundee. |
| [Update Coupon](actions/update-coupon.md) | PUT | Updates an existing coupon in Soundee. |

### Email Capture

| Action | Method | Description |
| --- | --- | --- |
| [List Email Captures](actions/list-email-captures.md) | GET | Retrieves captured email records from Soundee. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction record from Soundee. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves your transaction records from Soundee. |

