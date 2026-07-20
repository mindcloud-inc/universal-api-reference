# Selock: Unsubscribe Order Changes



```
DELETE https://connect.mindcloud.co/v1/universal/selock/latest/actions/unsubscribe-orders-change
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/selock/latest/actions/unsubscribe-orders-change?connectionId=$CONNECTION_ID&hookUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hookUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selock/latest/actions/unsubscribe-orders-change?${params}`, {
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
| `hookUrl` | string | yes | Webhook URL that Selock should stop calling. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "res": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `res` | boolean | True when the unsubscription was accepted. |

## Native endpoint

Through the native Selock API, this operation is `POST /zaiper/unsubscribe/orders_change/` (base URL `https://selock.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-orders-change.md) for the provider-specific parameters and requirements.

