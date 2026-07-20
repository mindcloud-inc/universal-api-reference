# Presenton: Unsubscribe All Webhook Subscriptions V3



```
DELETE https://connect.mindcloud.co/v1/universal/presenton/latest/actions/unsubscribe-all-webhook-subscriptions-v3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/unsubscribe-all-webhook-subscriptions-v3?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presenton/latest/actions/unsubscribe-all-webhook-subscriptions-v3?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Presenton API, this operation is `DELETE /api/v3/webhook/unsubscribe/all` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-all-webhook-subscriptions-v3.md) for the provider-specific parameters and requirements.

