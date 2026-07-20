# Salebot: Get Order Variables



```
GET https://connect.mindcloud.co/v1/universal/salebot/latest/actions/get-order-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/get-order-variables?connectionId=$CONNECTION_ID&clientId=1&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1",
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salebot/latest/actions/get-order-variables?${params}`, {
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
| `orderId` | number | yes | Existing Salebot order ID. |
| `variables[]` | array<string> | no | Variable names to return for the order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Salebot API, this operation is `POST /get_order_vars` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-variables.md) for the provider-specific parameters and requirements.

