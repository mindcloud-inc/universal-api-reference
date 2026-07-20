# SparkPost: Retrieve Webhook Event Documentation



```
GET https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-webhook-event-documentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-webhook-event-documentation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-webhook-event-documentation?${params}`, {
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
      "abTestEvent": {},
      "ingestEvent": {},
      "messageEvent": {},
      "relayEvent": {},
      "trackEvent": {},
      "unsubscribeEvent": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abTestEvent` | object |  |
| `ingestEvent` | object |  |
| `messageEvent` | object |  |
| `relayEvent` | object |  |
| `trackEvent` | object |  |
| `unsubscribeEvent` | object |  |

## Native endpoint

Through the native SparkPost API, this operation is `GET /webhooks/events/documentation` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-webhook-event-documentation.md) for the provider-specific parameters and requirements.

