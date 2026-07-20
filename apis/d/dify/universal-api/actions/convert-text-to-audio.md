# Dify: Convert Text to Audio

Creates audio from text in Dify.

```
POST https://connect.mindcloud.co/v1/universal/dify/latest/actions/convert-text-to-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dify/latest/actions/convert-text-to-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dify/latest/actions/convert-text-to-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | no | Message ID to convert to audio. |
| `text` | string | no | Text content to convert to audio. |
| `user` | string | no | User identifier. |
| `voice` | string | no | Voice to use for text-to-speech. |
| `streaming` | boolean | no | Whether to enable streaming audio response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dify API returns.

## Native endpoint

Through the native Dify API, this operation is `POST /text-to-audio` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-text-to-audio.md) for the provider-specific parameters and requirements.

