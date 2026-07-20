# OTO: Get Order Details

Retrieves order details from the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-order-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-order-details?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-order-details?${params}`, {
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
| `orderId` | string | yes | The merchant order identifier to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountDue": 1,
      "currency": "string",
      "customer": {},
      "destinationCity": "string",
      "id": 1,
      "items": [
        {}
      ],
      "orderDate": "string",
      "orderDocs": [
        {}
      ],
      "orderId": "string",
      "originCity": "string",
      "packageCount": 1,
      "packageWeight": 1,
      "paymentMethod": "string",
      "pickupLocation": "string",
      "status": "string",
      "statusHistory": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `amountDue` | number |  |
| `currency` | string |  |
| `customer` | object |  |
| `destinationCity` | string |  |
| `id` | number |  |
| `items` | array<object> |  |
| `orderDate` | string |  |
| `orderDocs` | array<object> |  |
| `orderId` | string |  |
| `originCity` | string |  |
| `packageCount` | number |  |
| `packageWeight` | number |  |
| `paymentMethod` | string |  |
| `pickupLocation` | string |  |
| `status` | string |  |
| `statusHistory` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native OTO API, this operation is `GET /orderDetails` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-details.md) for the provider-specific parameters and requirements.

