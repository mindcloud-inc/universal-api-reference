# Hy.page: Get Order



```
GET https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hypage/latest/actions/get-order?${params}`, {
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
| `id` | string | yes | Order ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "fulfillmentStatus": "string",
      "id": "string",
      "isTest": true,
      "itemCount": 1,
      "itemsData": {},
      "notes": "string",
      "orderNumber": "string",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "paymentPlatform": "string",
      "paymentStatus": "string",
      "people": {},
      "peopleId": "string",
      "shippingCarrier": "string",
      "trackingNumber": "string",
      "transactionId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `fulfillmentStatus` | string |  |
| `id` | string |  |
| `isTest` | boolean |  |
| `itemCount` | number |  |
| `itemsData` | object |  |
| `notes` | string |  |
| `orderNumber` | string |  |
| `paymentDate` | date |  |
| `paymentPlatform` | string |  |
| `paymentStatus` | string |  |
| `people` | object |  |
| `peopleId` | string |  |
| `shippingCarrier` | string |  |
| `trackingNumber` | string |  |
| `transactionId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Hy.page API, this operation is `GET /hyax-api/v1/orders/:id` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

