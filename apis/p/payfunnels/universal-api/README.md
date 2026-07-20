# <img src="https://images.mindcloud.co/apps/icons/payfunnels_1773856107928.png" alt="Payfunnels logo" width="28" height="28"> Payfunnels: Universal API

Collect payments, create payment links, and manage subscriptions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/payfunnels/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.payfunnels.com
- **Vendor API docs:** https://api.payfunnels.com/api/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Payments](actions/list-payments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Payment Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Plan Payment Link](actions/create-custom-plan-payment-link.md) | POST | Creates a custom plan payment link in Payfunnels. |
| [Create One-Time Payment Link](actions/create-one-time-payment-link.md) | POST | Creates a one-time payment link in Payfunnels. |
| [Create Pay What You Want Payment Link](actions/create-pay-what-you-want-payment-link.md) | POST | Creates a pay-what-you-want payment link in Payfunnels. |
| [Create Payment Plan Payment Link](actions/create-payment-plan-payment-link.md) | POST | Creates a payment plan link in Payfunnels. |
| [Create Recurring Payment Link](actions/create-recurring-payment-link.md) | POST | Creates a recurring payment link in Payfunnels. |
| [Get Payment Link](actions/get-payment-link.md) | GET | Retrieves a payment link from Payfunnels by ID. |
| [List Payment Links](actions/list-payment-links.md) | GET | Retrieves a list of payment links from Payfunnels. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a payment from Payfunnels by ID. |
| [List Payments](actions/list-payments.md) | GET | Retrieves a list of payments from Payfunnels. |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [Refund Payment](actions/refund-payment.md) | PUT | Updates a payment by refunding it in Payfunnels. |

### Setup Fee

| Action | Method | Description |
| --- | --- | --- |
| [Create Setup Fee](actions/create-setup-fee.md) | POST | Creates a new setup fee in Payfunnels. |
| [Delete Setup Fee](actions/delete-setup-fee.md) | DELETE | Deletes an existing setup fee from Payfunnels. |
| [Get Setup Fee](actions/get-setup-fee.md) | GET | Retrieves a setup fee from Payfunnels by ID. |
| [List Setup Fees](actions/list-setup-fees.md) | GET | Retrieves a list of setup fees from Payfunnels. |
| [Update Setup Fee](actions/update-setup-fee.md) | PUT | Updates an existing setup fee in Payfunnels. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Updates a subscription by cancelling it in Payfunnels. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from Payfunnels by ID. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves a list of subscriptions from Payfunnels. |
| [Pause Subscription](actions/pause-subscription.md) | PUT | Updates a subscription by pausing it in Payfunnels. |
| [Resume Subscription](actions/resume-subscription.md) | PUT | Updates a subscription by resuming it in Payfunnels. |

