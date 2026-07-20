# Shipday: Retrieve Order Details

Retrieves order details from Shipday.

```
GET https://connect.mindcloud.co/v1/universal/shipday/latest/actions/retrieve-order-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/retrieve-order-details?connectionId=$CONNECTION_ID&orderNumber=Test%20order%20002" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderNumber": "Test order 002"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipday/latest/actions/retrieve-order-details?${params}`, {
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
| `orderNumber` | string | yes | Shipday order reference used in the request path. Example: `Test order 002`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityLog": {
        "expectedDeliveryDate": "2026-05-07T12:00:00.000Z",
        "expectedDeliveryTime": "2026-05-07T12:00:00.000Z",
        "expectedPickupTime": "2026-05-07T12:00:00.000Z",
        "placementTime": "2026-05-07T12:00:00.000Z"
      },
      "costing": {
        "cashTip": 1,
        "deliveryFee": 1,
        "discountAmount": 1,
        "tax": 1,
        "tip": 1,
        "totalCost": 1
      },
      "customer": {
        "address": "string",
        "emailAddress": "ava@example.com",
        "id": 1,
        "latitude": 1,
        "longitude": 1,
        "name": "Ava Chen",
        "phoneNumber": "string"
      },
      "deliveryInstruction": "string",
      "distance": 1,
      "etaTime": "string",
      "idRequired": true,
      "orderId": 1,
      "orderItems": [
        {
          "detail": "string",
          "name": "Ava Chen",
          "quantity": 1,
          "unitPrice": 1
        }
      ],
      "orderNumber": "string",
      "orderSeqNum": 1,
      "orderStatus": {
        "accepted": true,
        "incomplete": true,
        "orderState": "string"
      },
      "orderStatusAdmin": "string",
      "parentId": 1,
      "pickupInstruction": "string",
      "restaurant": {
        "address": "string",
        "id": 1,
        "latitude": 1,
        "longitude": 1,
        "name": "Ava Chen",
        "phoneNumber": "string"
      },
      "schedule": true,
      "thirdPartyAssignedAnytime": true,
      "trackingLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityLog.expectedDeliveryDate` | date |  |
| `activityLog.expectedDeliveryTime` | date |  |
| `activityLog.expectedPickupTime` | date |  |
| `activityLog.placementTime` | date |  |
| `costing.cashTip` | number |  |
| `costing.deliveryFee` | number |  |
| `costing.discountAmount` | number |  |
| `costing.tax` | number |  |
| `costing.tip` | number |  |
| `costing.totalCost` | number |  |
| `customer.address` | string |  |
| `customer.emailAddress` | string |  |
| `customer.id` | number |  |
| `customer.latitude` | number |  |
| `customer.longitude` | number |  |
| `customer.name` | string |  |
| `customer.phoneNumber` | string |  |
| `deliveryInstruction` | string |  |
| `distance` | number |  |
| `etaTime` | string |  |
| `idRequired` | boolean |  |
| `orderId` | number |  |
| `orderItems[].detail` | string |  |
| `orderItems[].name` | string |  |
| `orderItems[].quantity` | number |  |
| `orderItems[].unitPrice` | number |  |
| `orderNumber` | string |  |
| `orderSeqNum` | number |  |
| `orderStatus.accepted` | boolean |  |
| `orderStatus.incomplete` | boolean |  |
| `orderStatus.orderState` | string |  |
| `orderStatusAdmin` | string |  |
| `parentId` | number |  |
| `pickupInstruction` | string |  |
| `restaurant.address` | string |  |
| `restaurant.id` | number |  |
| `restaurant.latitude` | number |  |
| `restaurant.longitude` | number |  |
| `restaurant.name` | string |  |
| `restaurant.phoneNumber` | string |  |
| `schedule` | boolean |  |
| `thirdPartyAssignedAnytime` | boolean |  |
| `trackingLink` | string |  |

## Native endpoint

Through the native Shipday API, this operation is `GET /orders/:orderNumber` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order-details.md) for the provider-specific parameters and requirements.

