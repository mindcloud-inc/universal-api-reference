# Lightfunnels: Create Shipping Rate Group



```
POST https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-shipping-rate-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-shipping-rate-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-shipping-rate-group', {
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
      "createShippingRateGroup": {
        "createdAt": "string",
        "id": "string",
        "rates": [
          {}
        ],
        "title": "string",
        "updatedAt": "string",
        "zones": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createShippingRateGroup.createdAt` | string |  |
| `createShippingRateGroup.id` | string |  |
| `createShippingRateGroup.rates` | array<object> |  |
| `createShippingRateGroup.title` | string |  |
| `createShippingRateGroup.updatedAt` | string |  |
| `createShippingRateGroup.zones` | array<object> |  |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipping-rate-group.md) for the provider-specific parameters and requirements.

