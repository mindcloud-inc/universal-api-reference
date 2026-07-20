# YouCan: Create Coupon

Creates a new coupon in YouCan.

```
POST https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-coupon', {
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
      "code": "string",
      "description": "string",
      "end_date": 1,
      "id": "string",
      "max_usage": 1,
      "start_date": 1,
      "status": "string",
      "type": 1,
      "type_text": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `description` | string |  |
| `end_date` | number |  |
| `id` | string |  |
| `max_usage` | number |  |
| `start_date` | number |  |
| `status` | string |  |
| `type` | number |  |
| `type_text` | string |  |
| `value` | number |  |

## Native endpoint

Through the native YouCan API, this operation is `POST /coupons` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-coupon.md) for the provider-specific parameters and requirements.

