# Speak Ai: Export Content

Creates a content export in Speak Ai.

```
POST https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/export-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/export-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaType": "string",
  "mediaId": "string",
  "fileType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/export-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaType": "string",
    "mediaId": "string",
    "fileType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaType` | string | yes | Resource type to export, such as media or text. |
| `mediaId` | string | yes | Speak Ai media or text identifier. |
| `fileType` | string | yes | Export format such as pdf, txt, docx, srt, or vtt. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isSpeakerNames` | boolean | no | Whether speaker names should be included in the export. Default: `true`. |
| `isTimeStamps` | boolean | no | Whether timestamps should be included in the export. Default: `true`. |
| `isInsightVisualized` | boolean | no | Whether insights should be visualized in the export when supported. Default: `true`. |
| `isRedacted` | boolean | no | Whether redacted content should be used in the export. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `POST /:mediaType/export/:mediaId/:fileType` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-content.md) for the provider-specific parameters and requirements.

