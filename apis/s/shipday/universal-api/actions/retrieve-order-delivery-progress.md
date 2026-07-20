# Shipday: Retrieve Order Delivery Progress

Retrieves order delivery progress from Shipday.

```
GET https://connect.mindcloud.co/v1/universal/shipday/latest/actions/retrieve-order-delivery-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/retrieve-order-delivery-progress?connectionId=$CONNECTION_ID&trackingId=cHB2eWZhcWE%3D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "cHB2eWZhcWE="
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipday/latest/actions/retrieve-order-delivery-progress?${params}`, {
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
| `trackingId` | string | yes | Shipday tracking token from the order tracking link. Example: `cHB2eWZhcWE=`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dynamicData": {
        "carrierLocation": {
          "latitude": 1,
          "longitude": 1
        },
        "detailEta": {
          "calprog": "string",
          "deliveryTime": 1,
          "estimatedTimeInMinutes": 1,
          "orderPosition": 1,
          "pickUpTime": 1,
          "startedOrder": 1,
          "travelDistance": 1,
          "travelDistanceTime": 1
        },
        "estimatedTimeInMinutes": "string",
        "orderStatus": {
          "arrivedTime": "2026-05-07T12:00:00.000Z",
          "deliveryTime": "2026-05-07T12:00:00.000Z",
          "failedDeliveryTime": "2026-05-07T12:00:00.000Z",
          "pickedTime": "2026-05-07T12:00:00.000Z",
          "startTime": "2026-05-07T12:00:00.000Z",
          "status": "string"
        }
      },
      "fixedData": {
        "carrier": {
          "id": 1,
          "imagePath": "string",
          "name": "Ava Chen",
          "phoneNumber": "string"
        },
        "customer": {
          "address": "string",
          "latitude": 1,
          "longitude": 1,
          "name": "Ava Chen"
        },
        "isExpired": true,
        "order": {
          "orderNumber": "string"
        },
        "restaurant": {
          "address": "string",
          "latitude": 1,
          "longitude": 1,
          "name": "Ava Chen"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dynamicData.carrierLocation.latitude` | number | Carrier latitude. |
| `dynamicData.carrierLocation.longitude` | number | Carrier longitude. |
| `dynamicData.detailEta.calprog` | string | Provider calculation-progress field. |
| `dynamicData.detailEta.deliveryTime` | number | Detailed delivery time contribution. |
| `dynamicData.detailEta.estimatedTimeInMinutes` | number | Detailed ETA minutes value. |
| `dynamicData.detailEta.orderPosition` | number | Order position in the route. |
| `dynamicData.detailEta.pickUpTime` | number | Detailed pickup time contribution. |
| `dynamicData.detailEta.startedOrder` | number | Started-order count. |
| `dynamicData.detailEta.travelDistance` | number | Detailed travel distance. |
| `dynamicData.detailEta.travelDistanceTime` | number | Detailed travel time contribution. |
| `dynamicData.estimatedTimeInMinutes` | string | High-level ETA minutes value. |
| `dynamicData.orderStatus.arrivedTime` | date | Arrival timestamp. |
| `dynamicData.orderStatus.deliveryTime` | date | Delivery timestamp. |
| `dynamicData.orderStatus.failedDeliveryTime` | date | Failed-delivery timestamp. |
| `dynamicData.orderStatus.pickedTime` | date | Pickup timestamp. |
| `dynamicData.orderStatus.startTime` | date | Tracking start timestamp. |
| `dynamicData.orderStatus.status` | string | Current delivery-progress status. |
| `fixedData.carrier.id` | number | Carrier identifier. |
| `fixedData.carrier.imagePath` | string | Carrier image path. |
| `fixedData.carrier.name` | string | Carrier name. |
| `fixedData.carrier.phoneNumber` | string | Carrier phone number. |
| `fixedData.customer.address` | string | Customer address. |
| `fixedData.customer.latitude` | number | Customer latitude. |
| `fixedData.customer.longitude` | number | Customer longitude. |
| `fixedData.customer.name` | string | Customer name. |
| `fixedData.isExpired` | boolean | Whether the tracking link is expired. |
| `fixedData.order.orderNumber` | string | Order number in the fixed tracking data. |
| `fixedData.restaurant.address` | string | Restaurant address. |
| `fixedData.restaurant.latitude` | number | Restaurant latitude. |
| `fixedData.restaurant.longitude` | number | Restaurant longitude. |
| `fixedData.restaurant.name` | string | Restaurant name. |

## Native endpoint

Through the native Shipday API, this operation is `GET /order/progress/:trackingId` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order-delivery-progress.md) for the provider-specific parameters and requirements.

