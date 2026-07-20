# Hyperstack Certificates: Unsubscribe from Webhook



```
DELETE https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/unsubscribe-from-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/unsubscribe-from-webhook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/unsubscribe-from-webhook?${params}`, {
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Confirmation message returned by Hyperstack. |
| `success` | boolean | Indicates whether the webhook subscription was successfully removed. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `POST /webhook/unsubscribe` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-from-webhook.md) for the provider-specific parameters and requirements.

