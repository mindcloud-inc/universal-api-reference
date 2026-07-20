# Bluesky: List Activity Subscriptions

Retrieves accounts the current Bluesky account subscribes to for notifications.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/list-activity-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/list-activity-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/list-activity-subscriptions?${params}`, {
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
      "cursor": "string",
      "subscriptions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `subscriptions` | array<object> |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.notification.listActivitySubscriptions` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activity-subscriptions.md) for the provider-specific parameters and requirements.

