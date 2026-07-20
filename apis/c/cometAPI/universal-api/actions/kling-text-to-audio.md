# CometAPI: Kling Text To Audio

Creates audio from text with Kling in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-text-to-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-text-to-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "duration": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-text-to-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "duration": "string",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duration` | string | yes | Audio duration. |
| `prompt` | string | yes | Text to audio prompt. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `task_id` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /kling/v1/audio/text-to-audio` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/kling-text-to-audio.md) for the provider-specific parameters and requirements.

