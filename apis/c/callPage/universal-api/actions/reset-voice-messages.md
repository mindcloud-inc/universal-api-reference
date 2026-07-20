# CallPage: Reset Voice Messages

Deletes all voice messages from CallPage.

```
DELETE https://connect.mindcloud.co/v1/universal/callPage/latest/actions/reset-voice-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/reset-voice-messages?connectionId=$CONNECTION_ID&widgetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "widgetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/reset-voice-messages?${params}`, {
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
| `widgetId` | number | yes | The widget identifier. |
| `messageId` | list<string> | no | The voice message identifier. One of: `client.end_failed`, `client.end_success`, `client.start`, `manager.start`, `manager.start_manual`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CallPage API returns.

## Native endpoint

Through the native CallPage API, this operation is `POST /voice/reset` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-voice-messages.md) for the provider-specific parameters and requirements.

