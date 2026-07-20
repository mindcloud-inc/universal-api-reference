# Lexware Office: Create Invoice

Creates a new invoice in Lexware Office.

```
POST https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voucherDate": "2026-05-07T12:00:00.000Z",
  "address": {},
  "lineItems[]": [
    {}
  ],
  "totalPrice": {},
  "taxConditions": {},
  "shippingConditions": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voucherDate": "2026-05-07T12:00:00.000Z",
    "address": {},
    "lineItems[]": [{}],
    "totalPrice": {},
    "taxConditions": {},
    "shippingConditions": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voucherDate` | date | yes | RFC 3339 timestamp for the invoice date. |
| `address` | object | yes | JSON object for the invoice recipient address. |
| `lineItems[]` | array<object> | yes | JSON array of invoice line item objects. |
| `totalPrice` | object | yes | JSON object for the invoice total price. |
| `taxConditions` | object | yes | JSON object describing invoice tax conditions. |
| `shippingConditions` | object | yes | JSON object describing invoice shipping conditions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `finalize` | boolean | no | Set to true to create an open invoice instead of the default draft invoice. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "resourceUri": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date |  |
| `id` | string |  |
| `resourceUri` | string |  |
| `updatedDate` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Lexware Office API, this operation is `POST /v1/invoices` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

