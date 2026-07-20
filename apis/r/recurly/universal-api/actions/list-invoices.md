# Recurly: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recurly `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beginTime` | string | no |  |
| `endTime` | string | no |  |
| `ids` | string | no |  |
| `state` | string | no | One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `type` | string | no | One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "address": {},
      "balance": 1,
      "billingInfoId": "string",
      "businessEntityId": "string",
      "closedAt": "2026-05-07T12:00:00.000Z",
      "collectionMethod": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditPayments": [
        {}
      ],
      "currency": "string",
      "customerNotes": "string",
      "discount": 1,
      "dueAt": "2026-05-07T12:00:00.000Z",
      "dunningCampaignId": "string",
      "dunningEventsSent": 1,
      "finalDunningEvent": true,
      "gatewayCode": "string",
      "hasMoreLineItems": true,
      "id": "string",
      "lineItems": [
        {}
      ],
      "netTerms": 1,
      "netTermsType": "string",
      "number": "string",
      "object": "string",
      "origin": "string",
      "paid": 1,
      "poNumber": "string",
      "previousInvoiceId": "string",
      "referenceOnlyCurrencyConversion": {},
      "refundableAmount": 1,
      "shippingAddress": {},
      "state": "string",
      "subscriptionIds": [
        "string"
      ],
      "subtotal": 1,
      "subtotalAfterDiscount": 1,
      "tax": 1,
      "taxInfo": {},
      "termsAndConditions": "string",
      "total": 1,
      "transactions": [
        {}
      ],
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usedTaxService": true,
      "uuid": "string",
      "vatNumber": "string",
      "vatReverseChargeNotes": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `address` | object |  |
| `balance` | number |  |
| `billingInfoId` | string |  |
| `businessEntityId` | string |  |
| `closedAt` | date |  |
| `collectionMethod` | string |  |
| `createdAt` | date |  |
| `creditPayments` | array<object> |  |
| `currency` | string |  |
| `customerNotes` | string |  |
| `discount` | number |  |
| `dueAt` | date |  |
| `dunningCampaignId` | string |  |
| `dunningEventsSent` | number |  |
| `finalDunningEvent` | boolean |  |
| `gatewayCode` | string |  |
| `hasMoreLineItems` | boolean |  |
| `id` | string |  |
| `lineItems` | array<object> |  |
| `netTerms` | number |  |
| `netTermsType` | string |  |
| `number` | string |  |
| `object` | string |  |
| `origin` | string |  |
| `paid` | number |  |
| `poNumber` | string |  |
| `previousInvoiceId` | string |  |
| `referenceOnlyCurrencyConversion` | object |  |
| `refundableAmount` | number |  |
| `shippingAddress` | object |  |
| `state` | string |  |
| `subscriptionIds` | array<string> |  |
| `subtotal` | number |  |
| `subtotalAfterDiscount` | number |  |
| `tax` | number |  |
| `taxInfo` | object |  |
| `termsAndConditions` | string |  |
| `total` | number |  |
| `transactions` | array<object> |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `usedTaxService` | boolean |  |
| `uuid` | string |  |
| `vatNumber` | string |  |
| `vatReverseChargeNotes` | string |  |

## Native endpoint

Through the native Recurly API, this operation is `GET /invoices` (base URL `https://v3.recurly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

