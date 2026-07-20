# <img src="https://images.mindcloud.co/apps/icons/bridge_1774471128492.png" alt="Bridge logo" width="28" height="28"> Bridge: Universal API

Initiate payments and synchronize banking data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bridge/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bridgeapi.io
- **Vendor API docs:** https://docs.bridgeapi.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Providers](actions/list-providers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/list-providers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Bridge. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Bridge. |

### Account Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Accounts Information](actions/get-accounts-information.md) | GET | Retrieves account identity information from Bridge. |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create Production Applications](actions/create-production-applications.md) | POST | Creates production applications in Bridge. |

### Authorization Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Authorization Token](actions/create-authorization-token.md) | POST | Creates a user authorization token in Bridge. |

### Beneficiary

| Action | Method | Description |
| --- | --- | --- |
| [List Beneficiaries](actions/list-beneficiaries.md) | GET | Retrieves beneficiaries from Bridge. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Bridge. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Bridge. |

### Connect Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Connect Session](actions/create-connect-session.md) | POST | Creates a connect session in Bridge. |

### Guidance Consent

| Action | Method | Description |
| --- | --- | --- |
| [Collect User Consent for Guidance Services](actions/collect-user-consent-for-guidance-services.md) | POST | Collects user consent for guidance services in Bridge. |
| [Get Financial Guidance Health for User](actions/get-financial-guidance-health-for-user.md) | GET | Retrieves financial guidance for a user in Bridge. |

### Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get Insights](actions/get-insights.md) | GET | Retrieves transaction insights from Bridge. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an item from Bridge. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from Bridge. |
| [List Items](actions/list-items.md) | GET | Retrieves items from Bridge. |

### Payment Consent

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Consent](actions/create-payment-consent.md) | POST | Creates a payment consent in Bridge. |

### Payment Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Link](actions/create-payment-link.md) | POST | Creates a payment link in Bridge. |
| [Get Payment Link](actions/get-payment-link.md) | GET | Retrieves a payment link from Bridge. |
| [List Payment Links](actions/list-payment-links.md) | GET | Retrieves payment links from Bridge. |
| [Revoke payment link](actions/revoke-payment-link.md) | PUT | Revokes a payment link in Bridge. |

### Payment Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Request](actions/create-payment-request.md) | POST | Creates a payment request in Bridge. |
| [Get Payment Request](actions/get-payment-request.md) | GET | Retrieves a payment request from Bridge. |
| [List Payment Requests](actions/list-payment-requests.md) | GET | Retrieves payment requests from Bridge. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [Create Payout](actions/create-payout.md) | POST | Creates a payout in Bridge. |
| [Get Payout](actions/get-payout.md) | GET | Retrieves a payout from Bridge. |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves payouts from Bridge. |

### Provider

| Action | Method | Description |
| --- | --- | --- |
| [Get Provider](actions/get-provider.md) | GET | Retrieves a provider from Bridge. |
| [List Providers](actions/list-providers.md) | GET | Retrieves supported providers from Bridge. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST | Creates a refund in Bridge. |
| [Get Refund](actions/get-refund.md) | GET | Retrieves a refund from Bridge. |
| [List Refunds](actions/list-refunds.md) | GET | Retrieves refunds from Bridge. |

### Stock

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock](actions/get-stock.md) | GET | Retrieves a stock from Bridge. |
| [List Stocks](actions/list-stocks.md) | GET | Retrieves stocks from Bridge. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Bridge. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from Bridge. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a user in Bridge. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Bridge. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Bridge. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Bridge. |

### User Management Session

| Action | Method | Description |
| --- | --- | --- |
| [Create User Management Session](actions/create-user-management-session.md) | POST | Creates a user management session in Bridge. |

