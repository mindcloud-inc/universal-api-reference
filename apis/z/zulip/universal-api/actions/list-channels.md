# Zulip: List Channels

Retrieves all channels available in Zulip.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-channels?${params}`, {
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
      "streams": [
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
| `msg` | string |  |
| `result` | string |  |
| `streams` | array<object> |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /streams` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

