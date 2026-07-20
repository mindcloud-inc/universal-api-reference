# Lightfunnels: Create App Charge



```
POST https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-app-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-app-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-app-charge', {
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
      "createAppCharge": {
        "appCharge": {
          "id": "string",
          "name": "Ava Chen",
          "price": 1,
          "startedAt": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createAppCharge` | object | Created app charge payload. |
| `createAppCharge.appCharge` | object | Created app charge. |
| `createAppCharge.appCharge.id` | string | App charge id. |
| `createAppCharge.appCharge.name` | string | App charge name. |
| `createAppCharge.appCharge.price` | number | App charge price. |
| `createAppCharge.appCharge.startedAt` | string | Charge start time. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-app-charge.md) for the provider-specific parameters and requirements.

