# WEBLUCY: Get Order

Retrieves an order from WEBLUCY.

```
GET https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-order?${params}`, {
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
| `id` | string | yes | The order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalFields": [
        {}
      ],
      "billingAddress": {},
      "contactId": 1,
      "created": 1,
      "customerEmail": "ava@example.com",
      "customerName": "Ava Chen",
      "discountAmount": 1,
      "discountCode": "string",
      "discountType": "string",
      "id": 1,
      "invoiceNo": 1,
      "items": [
        {}
      ],
      "memberId": 1,
      "notes": [
        {}
      ],
      "paid": true,
      "paymentMethod": "string",
      "shippingAddress": {},
      "shippingAmount": 1,
      "shippingName": "Ava Chen",
      "shippingRequired": true,
      "status": "string",
      "subTotal": 1,
      "tags": [
        "string"
      ],
      "taxes": [
        {}
      ],
      "total": 1,
      "transactionId": "string",
      "weight": 1,
      "weightUnit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalFields` | array<object> |  |
| `billingAddress` | object |  |
| `contactId` | number |  |
| `created` | number |  |
| `customerEmail` | string |  |
| `customerName` | string |  |
| `discountAmount` | number |  |
| `discountCode` | string |  |
| `discountType` | string |  |
| `id` | number |  |
| `invoiceNo` | number |  |
| `items` | array<object> |  |
| `memberId` | number |  |
| `notes` | array<object> |  |
| `paid` | boolean |  |
| `paymentMethod` | string |  |
| `shippingAddress` | object |  |
| `shippingAmount` | number |  |
| `shippingName` | string |  |
| `shippingRequired` | boolean |  |
| `status` | string |  |
| `subTotal` | number |  |
| `tags` | array<string> |  |
| `taxes` | array<object> |  |
| `total` | number |  |
| `transactionId` | string |  |
| `weight` | number |  |
| `weightUnit` | string |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `GET /orders/{id}` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

