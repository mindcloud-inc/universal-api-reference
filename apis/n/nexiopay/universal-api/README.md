# <img src="https://images.mindcloud.co/apps/icons/nexiopay_1776873155221.png" alt="Nexiopay logo" width="28" height="28"> Nexiopay: Universal API

Nexiopay provides payment processing, tokenization, terminal, alternative payment method, reporting, and payout APIs for merchants using the Nexio platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nexiopay/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nex.io
- **Vendor API docs:** https://docs.nexiopay.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Who am I](actions/who-am-i.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/who-am-i?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Alternative Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Capture an APM transaction](actions/capture-an-apm-transaction.md) | PUT |  |
| [Create APM one-time-use token](actions/create-apm-one-time-use-token.md) | POST |  |
| [Get APM iframe](actions/get-apm-iframe.md) | GET |  |
| [Refund an APM transaction](actions/refund-an-apm-transaction.md) | POST |  |
| [Run APM transaction](actions/run-apm-transaction.md) | POST |  |
| [View APM transaction async status](actions/view-apm-transaction-async-status.md) | GET |  |
| [Void an APM transaction](actions/void-an-apm-transaction.md) | PUT |  |

### Ecommerce

| Action | Method | Description |
| --- | --- | --- |
| [Capture a transaction](actions/capture-a-transaction.md) | PUT |  |
| [Create one-time-use token](actions/create-one-time-use-token.md) | POST |  |
| [Delete card tokens](actions/delete-card-tokens.md) | DELETE |  |
| [Refund a transaction](actions/refund-a-transaction.md) | POST |  |
| [Run card transaction](actions/run-card-transaction.md) | POST |  |
| [Run card transaction with iframe](actions/run-card-transaction-with-iframe.md) | GET |  |
| [Run echeck transaction](actions/run-echeck-transaction.md) | POST |  |
| [Run echeck transaction with iframe](actions/run-echeck-transaction-with-iframe.md) | GET |  |
| [Save card token](actions/save-card-token.md) | POST |  |
| [Save card token with iframe](actions/save-card-token-with-iframe.md) | GET |  |
| [Save echeck token](actions/save-echeck-token.md) | POST |  |
| [Save echeck token with iframe](actions/save-echeck-token-with-iframe.md) | GET |  |
| [Update card token](actions/update-card-token.md) | PUT |  |
| [View card token details](actions/view-card-token-details.md) | GET |  |
| [View card tokens](actions/view-card-tokens.md) | GET |  |
| [View currency conversion rates](actions/view-currency-conversion-rates.md) | GET |  |
| [View echeck token details](actions/view-echeck-token-details.md) | GET |  |
| [View surcharge recommendation](actions/view-surcharge-recommendation.md) | GET |  |
| [View transaction async status](actions/view-transaction-async-status.md) | GET |  |
| [Void a transaction](actions/void-a-transaction.md) | PUT |  |

### Merchant Service

| Action | Method | Description |
| --- | --- | --- |
| [View merchants by ID](actions/view-merchants-by-id.md) | GET |  |

### Payouts

| Action | Method | Description |
| --- | --- | --- |
| [View payouts](actions/view-payouts.md) | GET |  |

### Recipients

| Action | Method | Description |
| --- | --- | --- |
| [View recipients](actions/view-recipients.md) | GET |  |

### Retail

| Action | Method | Description |
| --- | --- | --- |
| [Create simple login](actions/create-simple-login.md) | POST |  |
| [Deregister terminal](actions/deregister-terminal.md) | DELETE |  |
| [Pair terminal](actions/pair-terminal.md) | POST |  |
| [Process transaction from terminal](actions/process-transaction-from-terminal.md) | POST |  |
| [Register terminal](actions/register-terminal.md) | POST |  |
| [View terminal list](actions/view-terminal-list.md) | GET |  |
| [View terminal transaction status](actions/view-terminal-transaction-status.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [View transaction by payment ID](actions/view-transaction-by-payment-id.md) | GET |  |
| [View transactions](actions/view-transactions.md) | GET |  |

### User Management

| Action | Method | Description |
| --- | --- | --- |
| [Who am I](actions/who-am-i.md) | GET |  |

