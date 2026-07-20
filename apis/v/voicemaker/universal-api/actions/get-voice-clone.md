# Voicemaker: Get Voice Clone

Retrieves a single voice clone from Voicemaker.

```
GET https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/get-voice-clone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/get-voice-clone?connectionId=$CONNECTION_ID&voiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "voiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/get-voice-clone?${params}`, {
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
| `voiceId` | string | yes | Voice clone ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Voicemaker API, this operation is `GET api/v1/voice-clones/{VoiceId}` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-voice-clone.md) for the provider-specific parameters and requirements.

