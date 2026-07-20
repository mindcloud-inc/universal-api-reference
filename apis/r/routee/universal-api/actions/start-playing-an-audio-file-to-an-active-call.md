# Routee: Start playing an audio file to an active call

Starts playing an audio file to an active call in Routee.

```
PUT https://connect.mindcloud.co/v1/universal/routee/latest/actions/start-playing-an-audio-file-to-an-active-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/routee/latest/actions/start-playing-an-audio-file-to-an-active-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "fileURL": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/start-playing-an-audio-file-to-an-active-call', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "fileURL": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The id of the voice call |
| `fileURL` | string | yes | The url of the wav file to play |
| `multiplex` | boolean | no | When set to true, the original audio is mixed together with the played file. Default value false |

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

Through the native Routee API, this operation is `POST /voice/conversation/:messageId/file` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-playing-an-audio-file-to-an-active-call.md) for the provider-specific parameters and requirements.

