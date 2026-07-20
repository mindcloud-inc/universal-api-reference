# Fiserv: Universal API

Manage Fiserv payments, balances, transactions, payouts, and fees

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fiserv/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fiserv.com
- **Vendor API docs:** https://isvportal.fiserv.com/docs/payments-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Banking Hub Access Token](actions/get-banking-hub-access-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/get-banking-hub-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Banking Hub Access Token](actions/get-banking-hub-access-token.md) | GET | Retrieves a Banking Hub access token from Fiserv. |

### Business Payout

| Action | Method | Description |
| --- | --- | --- |
| [List Business Payouts](actions/list-business-payouts.md) | GET | Retrieves payouts for a business from Fiserv. |

### Checkout Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Checkout Session](actions/create-checkout-session.md) | POST | Creates a checkout session in Fiserv. |
| [Expire Checkout Session](actions/expire-checkout-session.md) | PUT | Expires a checkout session in Fiserv. |
| [Get Checkout Session](actions/get-checkout-session.md) | GET | Retrieves a checkout session from Fiserv. |
| [List Checkout Sessions](actions/list-checkout-sessions.md) | GET | Retrieves checkout sessions for an account from Fiserv. |
| [Update Checkout Session](actions/update-checkout-session.md) | PUT | Updates an existing checkout session in Fiserv. |

### Dispute

| Action | Method | Description |
| --- | --- | --- |
| [Get Dispute](actions/get-dispute.md) | GET | Retrieves detailed dispute information from Fiserv. |
| [List Disputes](actions/list-disputes.md) | GET | Retrieves disputes and dispute details from Fiserv. |

### Fee

| Action | Method | Description |
| --- | --- | --- |
| [Create Fee](actions/create-fee.md) | POST | Creates a fee for a merchant account in Fiserv. |
| [Get Fee](actions/get-fee.md) | GET | Retrieves detailed fee information from Fiserv. |
| [List Fees](actions/list-fees.md) | GET | Retrieves fees for a merchant account from Fiserv. |

### Fee Refund

| Action | Method | Description |
| --- | --- | --- |
| [Refund Adhoc Fee](actions/refund-adhoc-fee.md) | POST | Creates a refund for an adhoc fee in Fiserv. |

### Ledger Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Ledger Account Balances](actions/fetch-ledger-account-balances.md) | GET | Retrieves ledger account balances from Fiserv. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST | Creates a payment for a payment intent in Fiserv. |
| [Get Payment](actions/get-payment.md) | GET | Retrieves detailed payment information from Fiserv. |
| [List Payments For Payment Intent](actions/list-payments-for-payment-intent.md) | GET | Retrieves payments for a payment intent from Fiserv. |

### Payment Intent

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Payment Intent](actions/cancel-payment-intent.md) | PUT | Cancels a payment intent in Fiserv. |
| [Capture Payment Intent](actions/capture-payment-intent.md) | PUT | Captures a payment intent in Fiserv. |
| [Create Payment Intent](actions/create-payment-intent.md) | POST | Creates a payment intent in Fiserv. |
| [Get Payment Intent](actions/get-payment-intent.md) | GET | Retrieves a payment intent from Fiserv. |
| [List Payment Intents](actions/list-payment-intents.md) | GET | Retrieves payment intents for an account from Fiserv. |
| [Search Payment Intents](actions/search-payment-intents.md) | GET | Finds payment intents in Fiserv by filter criteria. |
| [Update Payment Intent](actions/update-payment-intent.md) | PUT | Updates an existing payment intent in Fiserv. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Method](actions/get-payment-method.md) | GET | Retrieves a payment method from Fiserv. |
| [Update Payment Method](actions/update-payment-method.md) | PUT | Updates an existing payment method in Fiserv. |

### Payment Method Intent

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Payment Method Intent](actions/cancel-payment-method-intent.md) | PUT | Cancels a payment method intent in Fiserv. |
| [Create Payment Method Intent](actions/create-payment-method-intent.md) | POST | Creates a payment method intent in Fiserv. |
| [Get Payment Method Intent](actions/get-payment-method-intent.md) | GET | Retrieves a payment method intent from Fiserv. |
| [List Payment Method Intents](actions/list-payment-method-intents.md) | GET | Retrieves payment method intents from Fiserv. |
| [Update Payment Method Intent](actions/update-payment-method-intent.md) | PUT | Updates an existing payment method intent in Fiserv. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [Get Payout](actions/get-payout.md) | GET | Retrieves detailed payout information from Fiserv. |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves payouts for an account from Fiserv. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST | Creates a refund for a payment intent in Fiserv. |
| [Get Refund](actions/get-refund.md) | GET | Retrieves detailed refund information from Fiserv. |

### Surcharge

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Surcharge](actions/calculate-surcharge.md) | POST | Calculates a surcharge for a payment in Fiserv. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves detailed transaction information from Fiserv. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions for an account from Fiserv. |
| [Search Transactions](actions/search-transactions.md) | GET | Finds transactions in Fiserv by filter criteria. |

### Transaction Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Transactions](actions/download-transactions.md) | GET | Downloads a list of transactions from Fiserv. |

### Unmatched Settlement

| Action | Method | Description |
| --- | --- | --- |
| [List Unmatched Settlements](actions/list-unmatched-settlements.md) | GET | Retrieves unmatched settlements for a partner from Fiserv. |

