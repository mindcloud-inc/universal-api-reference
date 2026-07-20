# timeBuzzer: List Webhook Configurations



```
GET https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/list-webhook-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a timeBuzzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/list-webhook-configurations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/list-webhook-configurations?${params}`, {
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
      "event": "string",
      "id": 1,
      "requestHeaders": [
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
| `active` | boolean | Whether the webhook is active. |
| `event` | string | Webhook event name. |
| `id` | number | Webhook ID. |
| `requestHeaders` | array<object> | Configured request headers sent with the webhook. |
| `url` | string | Webhook target URL. |

## Native endpoint

Through the native timeBuzzer API, this operation is `GET /open-api/webhooks` (base URL `https://my.timebuzzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-configurations.md) for the provider-specific parameters and requirements.

