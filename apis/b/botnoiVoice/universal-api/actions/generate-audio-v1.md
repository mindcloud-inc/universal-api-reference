# Botnoi Voice: Generate Audio V1

Generates audio with Botnoi Voice V1.

```
POST https://connect.mindcloud.co/v1/universal/botnoiVoice/latest/actions/generate-audio-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botnoi Voice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botnoiVoice/latest/actions/generate-audio-v1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "speaker": "string",
  "typeMedia": "mp3"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botnoiVoice/latest/actions/generate-audio-v1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "speaker": "string",
    "typeMedia": "mp3"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | Text to convert into speech audio. |
| `speaker` | string | yes | Speaker identifier to use for voice generation. |
| `typeMedia` | string | yes | Output media format for the generated audio. Default: `mp3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `volume` | number | no | Volume level for the generated audio. Default: `100`. |
| `speed` | number | no | Playback speed for the generated audio. Default: `1`. |
| `saveFile` | boolean | no | Whether Botnoi should save the generated file. Default: `true`. |
| `language` | string | no | Language code for synthesis. Default: `th`. |
| `page` | string | no | Generation page context expected by the API. Default: `user`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioUrl": "https://example.com",
      "point": 1,
      "text": "string",
      "userMonthlyPoint": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioUrl` | string | URL for the generated audio file. |
| `point` | number | Point cost for the generated request. |
| `text` | string | Generated text returned by Botnoi Voice. |
| `userMonthlyPoint` | number | Remaining monthly point balance returned by the API. |

## Native endpoint

Through the native Botnoi Voice API, this operation is `POST /openapi/v1/generate_audio` (base URL `https://api-voice.botnoi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-audio-v1.md) for the provider-specific parameters and requirements.

