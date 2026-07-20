# TimelinesAI: Get Message Reactions

Retrieves reactions for a TimelinesAI message.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-message-reactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-message-reactions?connectionId=$CONNECTION_ID&messageUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-message-reactions?${params}`, {
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
| `messageUid` | string | yes | UID of the message in the TimelinesAI workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
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
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /messages/{message_uid}/reactions` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-reactions.md) for the provider-specific parameters and requirements.

