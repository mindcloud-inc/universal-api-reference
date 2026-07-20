# AntsRoute: Create Service/Delivery/Collect in Basket

Creates a new basket order in AntsRoute.

```
POST https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/create-service-delivery-collect-in-basket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AntsRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/create-service-delivery-collect-in-basket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer.address": "string",
  "customer.lastName": "Chen",
  "customer.latitude": 1,
  "customer.longitude": 1,
  "dueDate": "string",
  "duration": 1,
  "openDate": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/create-service-delivery-collect-in-basket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer.address": "string",
    "customer.lastName": "Chen",
    "customer.latitude": 1,
    "customer.longitude": 1,
    "dueDate": "string",
    "duration": 1,
    "openDate": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer.address` | string | yes | Customer address. |
| `customer.firstName` | string | no | Customer first name. |
| `customer.id` | number | no | Existing customer identifier. |
| `customer.lastName` | string | yes | Customer last name. |
| `customer.latitude` | number | yes | Customer latitude. |
| `customer.longitude` | number | yes | Customer longitude. |
| `dueDate` | string | yes | Order due date in `yyyy-MM-dd` format. |
| `duration` | number | yes | Planned service duration in minutes. |
| `externalId` | string | no | Unique external order identifier. |
| `openDate` | string | yes | Order open date in `yyyy-MM-dd` format. |
| `type` | string | yes | Order type, for example SERVICE. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AntsRoute API returns.

## Native endpoint

Through the native AntsRoute API, this operation is `POST /capi/order/basket` (base URL `https://app.antsroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service-delivery-collect-in-basket.md) for the provider-specific parameters and requirements.

