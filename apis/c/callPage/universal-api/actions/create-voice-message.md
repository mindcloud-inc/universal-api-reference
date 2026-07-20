# CallPage: Create Voice Message

Creates a new voice message in CallPage.

```
POST https://connect.mindcloud.co/v1/universal/callPage/latest/actions/create-voice-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/create-voice-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "widgetId": 1,
  "messageId": "client.end_failed",
  "enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callPage/latest/actions/create-voice-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "widgetId": 1,
    "messageId": "client.end_failed",
    "enabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `widgetId` | number | yes | The widget identifier. |
| `messageId` | list<string> | yes | The voice message identifier. One of: `client.end_failed`, `client.end_success`, `client.start`, `manager.start`, `manager.start_manual`. |
| `enabled` | boolean | yes | Whether the voice message should be enabled. |
| `file` | string | no | A public URL to an audio file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | The created custom voice message identifier. |

## Native endpoint

Through the native CallPage API, this operation is `POST /voice/create` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voice-message.md) for the provider-specific parameters and requirements.

