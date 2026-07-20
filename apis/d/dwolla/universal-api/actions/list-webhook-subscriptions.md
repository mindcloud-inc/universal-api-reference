# Dwolla: List Webhook Subscriptions

Retrieves a list of webhook subscriptions from Dwolla.

```
GET https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/list-webhook-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/list-webhook-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/list-webhook-subscriptions?${params}`, {
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
      "_embedded": {},
      "_links": {},
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object | Embedded webhook subscription rows returned by Dwolla. |
| `_links` | object | HAL links for the webhook subscription collection. |
| `total` | number | Total number of matching webhook subscriptions. |

## Native endpoint

Through the native Dwolla API, this operation is `GET /webhook-subscriptions` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-subscriptions.md) for the provider-specific parameters and requirements.

