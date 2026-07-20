# Routee: Stop playing a text-to-speech message to an active call

Stops playing a text-to-speech message to an active call in Routee.

```
DELETE https://connect.mindcloud.co/v1/universal/routee/latest/actions/stop-playing-a-text-to-speech-message-to-an-active-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/routee/latest/actions/stop-playing-a-text-to-speech-message-to-an-active-call?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/stop-playing-a-text-to-speech-message-to-an-active-call?${params}`, {
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
| `messageId` | string | yes | The id of the voice call |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "message": "string",
      "messageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `message` | string |  |
| `messageId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `DELETE /voice/conversation/:messageId/talk` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-playing-a-text-to-speech-message-to-an-active-call.md) for the provider-specific parameters and requirements.

