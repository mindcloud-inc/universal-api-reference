# JoggAI: Create Video with Template



```
POST https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-video-with-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-video-with-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": 1,
  "voiceLanguage": "string",
  "variables[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-video-with-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": 1,
    "voiceLanguage": "string",
    "variables[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | number | yes |  |
| `voiceLanguage` | string | yes |  |
| `variables[]` | array<object> | yes |  |
| `videoName` | string | no |  |
| `avatarId` | number | no |  |
| `avatarType` | number | no |  |
| `voiceId` | string | no |  |
| `captionsEnabled` | boolean | no |  |
| `backgroundMusicId` | number | no |  |
| `disableRandomTrans` | boolean | no |  |
| `disableRandomMoving` | boolean | no |  |
| `disableTrans` | boolean | no |  |
| `disableMoving` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `videoId` | string | Created template video ID |

## Native endpoint

Through the native JoggAI API, this operation is `POST /v2/create_video_with_template` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video-with-template.md) for the provider-specific parameters and requirements.

