# iPaymu: Native API Reference

A consolidated summary of iPaymu's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://ipaymu.com/api-collection/
- **API base URL:** `https://my.ipaymu.com/api/v2`

## Authentication

### API Key

Connect with your iPaymu API key and merchant VA.

### Credentials

- **API Key:** `apiKey` · required
- **Merchant VA:** `merchantVa` · required · Your iPaymu merchant VA from the Integration page.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://storage.googleapis.com/ipaymu-docs/ipaymu-api/iPaymu-signature-documentation-v2.pdf)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate COD Shipping](actions/calculate-cod-shipping.md) | `POST /cod/shipping-calculate` | [docs](https://ipaymu.com/api-collection/) |
| [Check Balance](actions/check-balance.md) | `POST /balance` | [docs](https://ipaymu.com/api-collection/) |
| [Check Transaction](actions/check-transaction.md) | `POST /transaction` | [docs](https://ipaymu.com/api-collection/) |
| [Create Direct Payment](actions/create-direct-payment.md) | `POST /payment/direct` | [docs](https://ipaymu.com/api-collection/) |
| [Create Redirect Payment](actions/create-redirect-payment.md) | `POST /payment` | [docs](https://ipaymu.com/api-collection/) |
| [Download COD Label](actions/download-cod-label.md) | `GET /cod/download-label/:transaction_id` | [docs](https://ipaymu.com/api-collection/) |
| [Get COD Coverage Area](actions/get-cod-coverage-area.md) | `GET /cod/area` | [docs](https://ipaymu.com/api-collection/) |
| [List Payment Channels](actions/list-payment-channels.md) | `GET /payment-channels` | [docs](https://ipaymu.com/api-collection/) |
| [List Transaction History](actions/list-transaction-history.md) | `POST /history` | [docs](https://ipaymu.com/api-collection/) |
| [Request COD Pickup](actions/request-cod-pickup.md) | `POST /cod/pickup` | [docs](https://ipaymu.com/api-collection/) |
| [Track COD Shipment](actions/track-cod-shipment.md) | `POST /cod/tracking` | [docs](https://ipaymu.com/api-collection/) |
