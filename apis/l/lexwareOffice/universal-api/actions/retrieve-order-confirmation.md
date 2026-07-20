# Lexware Office: Retrieve Order Confirmation

Retrieves an order confirmation from Lexware Office.

```
GET https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-order-confirmation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-order-confirmation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-order-confirmation?${params}`, {
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
| `id` | string | yes | The Lexware order confirmation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "archived": true,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "deliveryTerms": "string",
      "electronicDocumentProfile": "string",
      "id": "string",
      "introduction": "string",
      "language": "string",
      "lineItems": [
        {}
      ],
      "organizationId": "string",
      "paymentConditions": {},
      "relatedVouchers": [
        {}
      ],
      "remark": "string",
      "shippingConditions": {},
      "taxAmounts": [
        {}
      ],
      "taxConditions": {},
      "title": "string",
      "totalPrice": {},
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "version": 1,
      "voucherDate": "2026-05-07T12:00:00.000Z",
      "voucherNumber": "string",
      "voucherStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `archived` | boolean |  |
| `createdDate` | date |  |
| `deliveryTerms` | string |  |
| `electronicDocumentProfile` | string |  |
| `id` | string |  |
| `introduction` | string |  |
| `language` | string |  |
| `lineItems` | array<object> |  |
| `organizationId` | string |  |
| `paymentConditions` | object |  |
| `relatedVouchers` | array<object> |  |
| `remark` | string |  |
| `shippingConditions` | object |  |
| `taxAmounts` | array<object> |  |
| `taxConditions` | object |  |
| `title` | string |  |
| `totalPrice` | object |  |
| `updatedDate` | date |  |
| `version` | number |  |
| `voucherDate` | date |  |
| `voucherNumber` | string |  |
| `voucherStatus` | string |  |

## Native endpoint

Through the native Lexware Office API, this operation is `GET /v1/order-confirmations/:id` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order-confirmation.md) for the provider-specific parameters and requirements.

