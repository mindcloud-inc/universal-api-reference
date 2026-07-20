# Lightfunnels: Create Bundle



```
POST https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-bundle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-bundle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-bundle', {
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
      "createPriceBundle": {
        "id": "string",
        "items": [
          {
            "label": "string"
          }
        ],
        "label": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createPriceBundle` | object | Created bundle. |
| `createPriceBundle.id` | string | Bundle id. |
| `createPriceBundle.items` | array<object> | Bundle items. |
| `createPriceBundle.items[].label` | string | Bundle item label. |
| `createPriceBundle.label` | string | Bundle label. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bundle.md) for the provider-specific parameters and requirements.

