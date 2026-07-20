# ClickMeeting: Download Chat Archive

Downloads a chat archive from ClickMeeting by session ID.

```
GET https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/download-chat-archive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickMeeting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/download-chat-archive?connectionId=$CONNECTION_ID&session_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "session_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickMeeting/latest/actions/download-chat-archive?${params}`, {
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
| `session_id` | number | yes | Session identifier used by the chat archive endpoint. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ClickMeeting API returns.

## Native endpoint

Through the native ClickMeeting API, this operation is `GET chats/{{session_id}}` (base URL `https://api.clickmeeting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-chat-archive.md) for the provider-specific parameters and requirements.

