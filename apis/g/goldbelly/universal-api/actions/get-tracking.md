# Goldbelly: Get Tracking



```
GET https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/get-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goldbelly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/get-tracking?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/get-tracking?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | Goldbelly order ID to retrieve tracking information for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "orderId": 1,
      "status": "string",
      "trackingNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `orderId` | number |  |
| `status` | string |  |
| `trackingNumber` | string |  |

## Native endpoint

Through the native Goldbelly API, this operation is `GET tracking/:order_id` (base URL `https://api.goldbelly.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracking.md) for the provider-specific parameters and requirements.

