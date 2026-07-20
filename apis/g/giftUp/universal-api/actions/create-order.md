# Gift Up: Create Order



```
POST https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaserName": "Ava Chen",
  "itemDetails[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "purchaserName": "Ava Chen",
    "itemDetails[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaserName` | string | yes |  |
| `purchaserEmail` | string | no |  |
| `disableAllEmails` | boolean | no | Default: `false`. |
| `orderDate` | date | no |  |
| `referrer` | string | no |  |
| `revenue` | number | no |  |
| `tip` | number | no |  |
| `serviceFee` | number | no |  |
| `discount` | number | no |  |
| `itemDetails[]` | array<object> | yes |  |
| `recipientDetails` | object | no |  |
| `customFields[]` | array<object> | no |  |
| `salesTaxes[]` | array<object> | no |  |
| `metadata` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customFields": [
        "string"
      ],
      "discount": 1,
      "downloadLinks": {},
      "fulfilments": [
        "string"
      ],
      "giftCards": [
        {}
      ],
      "id": "string",
      "metadata": {},
      "notes": [
        "string"
      ],
      "orderId": "string",
      "orderNumber": "string",
      "payment": {},
      "promotions": [
        "string"
      ],
      "purchaserEmail": "ava@example.com",
      "purchaserName": "Ava Chen",
      "referrer": "string",
      "revenue": 1,
      "salesTaxes": [
        "string"
      ],
      "selectedRecipient": "string",
      "serviceFee": 1,
      "shippingFee": 1,
      "tip": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `currency` | string |  |
| `customFields` | array<string> |  |
| `discount` | number |  |
| `downloadLinks` | object |  |
| `fulfilments` | array<string> |  |
| `giftCards` | array<object> |  |
| `id` | string |  |
| `metadata` | object |  |
| `notes` | array<string> |  |
| `orderId` | string |  |
| `orderNumber` | string |  |
| `payment` | object |  |
| `promotions` | array<string> |  |
| `purchaserEmail` | string |  |
| `purchaserName` | string |  |
| `referrer` | string |  |
| `revenue` | number |  |
| `salesTaxes` | array<string> |  |
| `selectedRecipient` | string |  |
| `serviceFee` | number |  |
| `shippingFee` | number |  |
| `tip` | number |  |

## Native endpoint

Through the native Gift Up API, this operation is `POST /orders` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

