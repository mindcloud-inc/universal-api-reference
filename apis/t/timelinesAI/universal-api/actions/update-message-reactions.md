# TimelinesAI: Update Message Reactions

Updates reactions on an existing TimelinesAI message.

```
PUT https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/update-message-reactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/update-message-reactions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageUid": "string",
  "reaction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/update-message-reactions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageUid": "string",
    "reaction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageUid` | string | yes | UID of the message in the TimelinesAI workspace. |
| `reaction` | string | yes | Reaction emoji to set for the message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "messageUid": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.messageUid` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `PATCH /messages/{message_uid}/reactions` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message-reactions.md) for the provider-specific parameters and requirements.

