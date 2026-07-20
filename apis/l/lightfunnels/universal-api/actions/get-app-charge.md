# Lightfunnels: Get App Charge



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/get-app-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/get-app-charge?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/get-app-charge?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "appCharge": {
        "id": "string",
        "name": "Ava Chen",
        "price": 1,
        "startedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appCharge` | object | App charge. |
| `appCharge.id` | string | App charge id. |
| `appCharge.name` | string | App charge name. |
| `appCharge.price` | number | App charge price. |
| `appCharge.startedAt` | string | Charge start time. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-charge.md) for the provider-specific parameters and requirements.

