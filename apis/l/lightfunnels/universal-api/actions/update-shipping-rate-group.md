# Lightfunnels: Update Shipping Rate Group



```
PUT https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/update-shipping-rate-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/update-shipping-rate-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/update-shipping-rate-group', {
  method: 'PUT',
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
      "updateShippingRateGroup": {
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
| `updateShippingRateGroup.createdAt` | string |  |
| `updateShippingRateGroup.id` | string |  |
| `updateShippingRateGroup.rates` | array<object> |  |
| `updateShippingRateGroup.title` | string |  |
| `updateShippingRateGroup.updatedAt` | string |  |
| `updateShippingRateGroup.zones` | array<object> |  |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shipping-rate-group.md) for the provider-specific parameters and requirements.

