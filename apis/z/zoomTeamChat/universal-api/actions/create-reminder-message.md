# Zoom Team Chat: Create Reminder Message



```
POST https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/create-reminder-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/create-reminder-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/create-reminder-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The unique identifier of the message. |
| `toContact` | string | no | The email address of the Zoom contact for the reminder. |
| `toChannel` | string | no | The ID of the Zoom channel for the reminder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message_id": "string",
      "to_channel": "string",
      "to_contact": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message_id` | string |  |
| `to_channel` | string |  |
| `to_contact` | string |  |

## Native endpoint

Through the native Zoom Team Chat API, this operation is `POST /chat/messages/:messageId/reminder` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reminder-message.md) for the provider-specific parameters and requirements.

