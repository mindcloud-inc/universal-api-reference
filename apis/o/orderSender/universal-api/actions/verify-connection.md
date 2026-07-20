# Order Sender: Verify Connection

Retrieves Order Sender account status and API access validity.

```
GET https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/verify-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/verify-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/verify-connection?${params}`, {
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
      "account": "string",
      "expire": "2026-05-07T12:00:00.000Z",
      "msg": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `expire` | date |  |
| `msg` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Order Sender API, this operation is `GET /op/check` (base URL `https://business.ordersender.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-connection.md) for the provider-specific parameters and requirements.

