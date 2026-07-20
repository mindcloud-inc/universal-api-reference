# DataForB2B: Get Webhook Subscription

Retrieves a webhook subscription from DataForB2B.

```
GET https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/get-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForB2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/get-webhook-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/get-webhook-subscription?${params}`, {
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
      "active": true,
      "created_at": "string",
      "event_types": [
        "string"
      ],
      "id": 1,
      "monitored_profiles": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created_at` | string |  |
| `event_types` | array<string> |  |
| `id` | number |  |
| `monitored_profiles` | array<object> |  |
| `url` | string |  |

## Native endpoint

Through the native DataForB2B API, this operation is `GET /webhooks` (base URL `https://api.dataforb2b.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-subscription.md) for the provider-specific parameters and requirements.

