# EenvoudigFactureren: Create Order

Creates a new order in EenvoudigFactureren.

```
POST https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/create-order', {
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
      "client_name": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "order_id": 1,
      "status": "string",
      "total": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_name` | string |  |
| `date` | date |  |
| `number` | string |  |
| `order_id` | number |  |
| `status` | string |  |
| `total` | number |  |
| `uri` | string |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `POST /orders` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

