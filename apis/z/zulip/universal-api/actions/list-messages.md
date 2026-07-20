# Zulip: List Messages

Retrieves messages from Zulip using specified filters.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/list-messages?${params}`, {
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
| `anchor` | string | no | Where to anchor the message query, for example newest or a message ID. |
| `numAfter` | number | no | How many messages to return after the anchor. |
| `numBefore` | number | no | How many messages to return before the anchor. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anchor": 1,
      "found_anchor": true,
      "found_newest": true,
      "found_oldest": true,
      "history_limited": true,
      "messages": [
        {}
      ],
      "msg": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anchor` | number |  |
| `found_anchor` | boolean |  |
| `found_newest` | boolean |  |
| `found_oldest` | boolean |  |
| `history_limited` | boolean |  |
| `messages` | array<object> |  |
| `msg` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /messages` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

