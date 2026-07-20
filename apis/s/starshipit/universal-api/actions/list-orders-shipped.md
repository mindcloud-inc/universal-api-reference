# Starshipit: List Orders (Shipped)



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-shipped
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-shipped?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-shipped?${params}`, {
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
| `sinceLastUpdated` | date | no | Show orders recently updated after date in UTC (date-time in RFC3339 format) |
| `idsOnly` | boolean | no | Show all unshipped order_ids |
| `limit` | number | no | Amount of results (default: 50) (maximum: 250) |
| `page` | number | no | Page to show (default: 1) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": [
        {
          "carrier": "string",
          "carrierName": "Ava Chen",
          "carrierServiceCode": "string",
          "carrierServiceName": "Ava Chen",
          "country": "string",
          "integrationSourceName": "Ava Chen",
          "manifestNumber": 1,
          "manifestSent": true,
          "name": "Ava Chen",
          "orderDate": "2026-05-07T12:00:00.000Z",
          "orderId": 1,
          "orderNumber": "string",
          "reference": "string",
          "shipmentType": "string",
          "shippedDate": "2026-05-07T12:00:00.000Z",
          "state": "string",
          "trackingFullStatus": "string",
          "trackingNumber": "string",
          "trackingShortStatus": "string",
          "writebackDetails": "string",
          "writebackStatus": "string"
        }
      ],
      "success": true,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orders` | array<object> |  |
| `orders[].carrier` | string |  |
| `orders[].carrierName` | string |  |
| `orders[].carrierServiceCode` | string |  |
| `orders[].carrierServiceName` | string |  |
| `orders[].country` | string |  |
| `orders[].integrationSourceName` | string |  |
| `orders[].manifestNumber` | number |  |
| `orders[].manifestSent` | boolean |  |
| `orders[].name` | string |  |
| `orders[].orderDate` | date |  |
| `orders[].orderId` | number |  |
| `orders[].orderNumber` | string |  |
| `orders[].reference` | string |  |
| `orders[].shipmentType` | string |  |
| `orders[].shippedDate` | date |  |
| `orders[].state` | string |  |
| `orders[].trackingFullStatus` | string |  |
| `orders[].trackingNumber` | string |  |
| `orders[].trackingShortStatus` | string |  |
| `orders[].writebackDetails` | string |  |
| `orders[].writebackStatus` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /orders/shipped` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders-shipped.md) for the provider-specific parameters and requirements.

