# Starshipit: List Orders (Printed or Unmanifested)



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-printed-or-unmanifested
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-printed-or-unmanifested?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-printed-or-unmanifested?${params}`, {
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
| `sinceCreatedDate` | date | no | Show shipments created after date in UTC (date-time in RFC3339 format) |
| `status` | string | no | The status of the shipments to return |
| `limit` | string | no | Amount of results (default: 50) (maximum: 250) |
| `page` | string | no | Page to show (default: 1) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": [
        {
          "carrierName": "Ava Chen",
          "carrierServiceCode": "string",
          "country": "string",
          "date": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "orderId": 1,
          "orderNumber": "string",
          "trackingNumbers": [
            "string"
          ]
        }
      ],
      "status": "string",
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
| `orders[].carrierName` | string |  |
| `orders[].carrierServiceCode` | string |  |
| `orders[].country` | string |  |
| `orders[].date` | date |  |
| `orders[].name` | string |  |
| `orders[].orderId` | number |  |
| `orders[].orderNumber` | string |  |
| `orders[].trackingNumbers` | array<string> |  |
| `status` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /orders/shipments` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders-printed-or-unmanifested.md) for the provider-specific parameters and requirements.

