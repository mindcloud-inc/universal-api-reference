# <img src="https://images.mindcloud.co/apps/icons/favicon-19_1775594536134.png" alt="aamarPay logo" width="28" height="28"> aamarPay: Universal API

Accept payments and verify transaction status with aamarPay

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aamarPay/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://aamarpay.com
- **Vendor API docs:** https://aamarpay.readme.io/reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Transaction](actions/search-transaction.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/search-transaction?connectionId=$CONNECTION_ID&requestId=1231231773" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Initiate Payment (Form Data)](actions/initiate-payment-form-data.md) | POST | Creates a payment request in aamarPay using form data. |
| [Initiate Payment (JSON)](actions/initiate-payment-json.md) | POST | Creates a payment request in aamarPay using JSON. |
| [Search Transaction](actions/search-transaction.md) | GET | Retrieves transaction details from aamarPay by merchant transaction ID. |

