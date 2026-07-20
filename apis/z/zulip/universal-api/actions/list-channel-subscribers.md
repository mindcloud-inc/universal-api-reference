# Zulip: List Channel Subscribers

Retrieves subscribers for a specific Zulip channel.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-channel-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-channel-subscribers?connectionId=$CONNECTION_ID&streamId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "streamId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-channel-subscribers?${params}`, {
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
| `streamId` | number | yes | The target channel ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "result": "string",
      "subscribers": [
        1
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
| `subscribers` | array<number> |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /streams/:stream_id/members` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-subscribers.md) for the provider-specific parameters and requirements.

