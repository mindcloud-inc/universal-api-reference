# Billforward: Universal API

Billforward: Manage subscriptions, billing, and customer accounts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/billforward/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.billforward.io/
- **Vendor API docs:** https://app.billforward.net/#/api/docs/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billforward/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in Billforward. |
| [Find Account By Email](actions/find-account-by-email.md) | GET | Finds an account in Billforward by email address. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Billforward. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Billforward. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in Billforward. |

### Credit Note

| Action | Method | Description |
| --- | --- | --- |
| [Add Credit To Account](actions/add-credit-to-account.md) | POST | Creates a new credit note for a Billforward account. |
| [Get Credit Note](actions/get-credit-note.md) | GET | Retrieves a credit note from Billforward. |
| [List Account Credit Notes](actions/list-account-credit-notes.md) | GET | Retrieves credit notes for a Billforward account. |
| [List Credit Notes](actions/list-credit-notes.md) | GET | Retrieves credit notes from Billforward. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Account Invoices](actions/list-account-invoices.md) | GET | Retrieves invoices for a Billforward account. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Billforward. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from Billforward. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves payment methods from Billforward. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Billforward. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Billforward. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Billforward. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves a profile from Billforward. |
| [List Profiles](actions/list-profiles.md) | GET | Retrieves profiles from Billforward. |
| [List Profiles By Account](actions/list-profiles-by-account.md) | GET | Retrieves profiles for a Billforward account. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Billforward. |

