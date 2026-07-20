# Zulip: Get Channel ID

Finds a Zulip channel ID by name.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-channel-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-channel-id?connectionId=$CONNECTION_ID&stream=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stream": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-channel-id?${params}`, {
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
| `stream` | string | yes | The name of the channel to access. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "result": "string",
      "stream_id": 1
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
| `stream_id` | number |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /get_stream_id` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-id.md) for the provider-specific parameters and requirements.

