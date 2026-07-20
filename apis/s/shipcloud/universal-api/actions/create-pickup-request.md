# Shipcloud: Create Pickup Request

Creates a new pickup request in Shipcloud.

```
POST https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-pickup-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-pickup-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-pickup-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "carrier_pickup_number": "string",
      "id": "string",
      "pickup_address": {},
      "pickup_time": {},
      "shipments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `carrier_pickup_number` | string |  |
| `id` | string |  |
| `pickup_address` | object |  |
| `pickup_time` | object |  |
| `shipments` | array<object> |  |

## Native endpoint

Through the native Shipcloud API, this operation is `POST /pickup_requests` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pickup-request.md) for the provider-specific parameters and requirements.

