# Zulip: Fetch Single Message

Retrieves a single Zulip message by ID.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/fetch-single-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/fetch-single-message?connectionId=$CONNECTION_ID&messageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/fetch-single-message?${params}`, {
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
| `messageId` | number | yes | The target message ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": {},
      "msg": "string",
      "raw_content": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | object |  |
| `msg` | string |  |
| `raw_content` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /messages/:message_id` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-single-message.md) for the provider-specific parameters and requirements.

