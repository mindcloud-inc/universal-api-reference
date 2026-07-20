# Envoice: Create Order

Creates a new order in Envoice.

```
POST https://connect.mindcloud.co/v1/universal/envoice/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currencyId": 1,
  "items": "string",
  "name": "Ava Chen",
  "status": "string",
  "totalAmount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currencyId": 1,
    "items": "string",
    "name": "Ava Chen",
    "status": "string",
    "totalAmount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currencyId` | number | yes | Currency identifier. |
| `items` | string | yes | JSON array of order item objects. |
| `name` | string | yes | Order name. |
| `orderBillingDetails` | string | no | JSON object with order billing details. |
| `orderShippingDetails` | string | no | JSON object with order shipping details. |
| `productId` | number | no | Product identifier for the order. |
| `shippingAmount` | number | no | Order shipping amount. |
| `status` | string | yes | Order status. |
| `subTotalAmount` | number | no | Order subtotal amount. |
| `taxAmount` | number | no | Order tax amount. |
| `totalAmount` | number | yes | Order total amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorMessages": [
        "string"
      ],
      "Id": 1,
      "IsFaulted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorMessages` | array<string> | Error messages returned by Envoice. |
| `Id` | number | Created order identifier. |
| `IsFaulted` | boolean | Whether the request failed. |

## Native endpoint

Through the native Envoice API, this operation is `POST order/new` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

