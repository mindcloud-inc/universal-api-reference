# Zulip: List Subscribed Channels

Retrieves subscribed channels for the requesting Zulip user.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-subscribed-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-subscribed-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-subscribed-channels?${params}`, {
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
      "msg": "string",
      "result": "string",
      "subscriptions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string |  |
| `result` | string |  |
| `subscriptions` | array |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /users/me/subscriptions` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribed-channels.md) for the provider-specific parameters and requirements.

