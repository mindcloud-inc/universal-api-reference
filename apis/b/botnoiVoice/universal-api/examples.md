# Botnoi Voice Universal API Examples

These examples use the MindCloud API key and Botnoi Voice connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Speakers

Retrieves speakers from Botnoi Voice V2.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botnoiVoice/latest/actions/list-speakers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botnoiVoice/latest/actions/list-speakers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [List Speakers action reference](actions/list-speakers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botnoiVoice/latest/actions/list-speakers).

## Generate Audio V1

Generates audio with Botnoi Voice V1.

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

Example response:

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

See the full [Generate Audio V1 action reference](actions/generate-audio-v1.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botnoiVoice/latest/actions/generate-audio-v1).
