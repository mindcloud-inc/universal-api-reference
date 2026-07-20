# Botnoi Voice: List Speakers V1

Retrieves speakers from Botnoi Voice V1.

```
GET https://connect.mindcloud.co/v1/universal/botnoiVoice/latest/actions/list-speakers-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botnoi Voice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botnoiVoice/latest/actions/list-speakers-v1?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botnoiVoice/latest/actions/list-speakers-v1?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ageStyle": "string",
      "audio": "string",
      "availableLanguage": [
        "string"
      ],
      "engAgeStyle": "string",
      "engGender": "string",
      "engName": "Ava Chen",
      "engSpeechStyle": [
        "string"
      ],
      "engSpeed": "string",
      "engVoiceStyle": [
        "string"
      ],
      "gender": "string",
      "image": "string",
      "language": "string",
      "price": 1,
      "speakerId": "string",
      "speechStyle": [
        "string"
      ],
      "speed": "string",
      "thaiName": "Ava Chen",
      "voiceStyle": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ageStyle` | string |  |
| `audio` | string |  |
| `availableLanguage` | array<string> |  |
| `engAgeStyle` | string |  |
| `engGender` | string |  |
| `engName` | string |  |
| `engSpeechStyle` | array<string> |  |
| `engSpeed` | string |  |
| `engVoiceStyle` | array<string> |  |
| `gender` | string |  |
| `image` | string |  |
| `language` | string |  |
| `price` | number |  |
| `speakerId` | string |  |
| `speechStyle` | array<string> |  |
| `speed` | string |  |
| `thaiName` | string |  |
| `voiceStyle` | array<string> |  |

## Native endpoint

Through the native Botnoi Voice API, this operation is `GET /openapi/v1/get_speaker_data` (base URL `https://api-voice.botnoi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-speakers-v1.md) for the provider-specific parameters and requirements.

