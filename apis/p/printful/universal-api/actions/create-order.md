# Printful: Create Order

Creates a new order in Printful.

```
POST https://connect.mindcloud.co/v1/universal/printful/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printful/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printful/latest/actions/create-order', {
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
      "created": 1,
      "external_id": "string",
      "id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `external_id` | string |  |
| `id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Printful API, this operation is `POST /orders` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

