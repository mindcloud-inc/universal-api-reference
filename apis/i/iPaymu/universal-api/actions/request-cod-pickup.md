# iPaymu: Request COD Pickup

Create an iPaymu cash-on-delivery pickup request.

```
POST https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/request-cod-pickup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/request-cod-pickup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transaction_id": "string",
  "pickup_date": "string",
  "pickup_time": "string",
  "pickup_vehicle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/request-cod-pickup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transaction_id": "string",
    "pickup_date": "string",
    "pickup_time": "string",
    "pickup_vehicle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transaction_id` | string | yes | COD transaction identifier. |
| `pickup_date` | string | yes | Pickup date in YYYY-MM-DD. |
| `pickup_time` | string | yes | Pickup time in HH:mm. |
| `pickup_vehicle` | string | yes | Pickup vehicle, for example Motor or Mobil. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iPaymu API returns.

## Native endpoint

Through the native iPaymu API, this operation is `POST /cod/pickup` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-cod-pickup.md) for the provider-specific parameters and requirements.

