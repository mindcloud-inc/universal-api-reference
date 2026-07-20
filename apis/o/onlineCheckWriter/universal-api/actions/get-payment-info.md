# OnlineCheckWriter: Get Payment Info

Retrieves the status and details of a specific payment.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-payment-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-payment-info?connectionId=$CONNECTION_ID&paymentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-payment-info?${params}`, {
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
| `paymentId` | string | yes | The payment identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnlineCheckWriter API returns.

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /send-payment/:paymentId/info` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-info.md) for the provider-specific parameters and requirements.

