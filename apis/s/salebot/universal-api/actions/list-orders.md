# Salebot: List Orders



```
GET https://connect.mindcloud.co/v1/universal/salebot/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/list-orders?connectionId=$CONNECTION_ID&clientId=1&orderStatus=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1",
  "orderStatus": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salebot/latest/actions/list-orders?${params}`, {
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
| `clientId` | number | yes | Existing Salebot client ID. |
| `orderStatus` | number | yes | 0 for active, 1 for won, 2 for lost orders. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        1
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<number> |  |
| `status` | string |  |

## Native endpoint

Through the native Salebot API, this operation is `GET /get_orders` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

