# CometAPI: Create Speech

Creates speech audio in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/create-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/create-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string",
  "model": "string",
  "voice": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/create-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string",
    "model": "string",
    "voice": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | Text to synthesize. |
| `model` | string | yes | Speech model ID. |
| `voice` | string | yes | Voice name to use for the audio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "fileContent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `fileContent` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /v1/audio/speech` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-speech.md) for the provider-specific parameters and requirements.

